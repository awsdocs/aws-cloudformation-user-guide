# Using AWS CloudFormation macros to perform custom processing on templates<a name="template-macros"></a>

Macros enable you to perform custom processing on templates, from simple actions like find\-and\-replace operations to extensive transformations of entire templates\. 

To get an idea of the breadth of possibilities, consider the `AWS::Include` and `AWS::Serverless` transforms, which are macros hosted by AWS CloudFormation:
+ `AWS::Include transform` enables you to insert boilerplate template snippets into your templates\.
+ `AWS::Serverless transform` takes an entire template written in the AWS Serverless Application Model \(AWS SAM\) syntax and transforms and expands it into a compliant AWS CloudFormation template\. \(For more information about serverless applications and AWS SAM, see [Deploying Lambda\-based applications](https://docs.aws.amazon.com/lambda/latest/dg/deploying-lambda-apps.html) in the *AWS Lambda Developer Guide*\.\)

## How AWS CloudFormation macros work<a name="template-macros-overview"></a>

There are two major steps to processing templates using macros: *creating* the macro itself, and then *using* the macro to perform processing on your templates\.

To create a macro definition, you need to create the following:
+ An AWS Lambda function to perform the template processing\. This Lambda function accepts either a snippet or an entire template, and any additional parameters that you define\. It returns the processed template snippet or the entire template as a response\.
+ A resource of type `[AWS::CloudFormation::Macro](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-macro.html)`, which enables users to call the Lambda function from within AWS CloudFormation templates\. This resource specifies the ARN of the Lambda function to invoke for this macro, and additional optional properties to assist with debugging\. To create this resource within an account, author a stack template that includes a `[AWS::CloudFormation::Macro](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-macro.html)` resource, and then create a stack from the template\.

To use a macro, reference the macro in your template:
+ To process a section, or *snippet*, of a template, reference the macro in a ``Fn::Transform`` function located relative to the template content you want to transform\. When using `Fn::Transform`, you can also pass any specified parameters it requires\.
+ To process an entire template, reference the macro in the [Transform](transform-section-structure.md) section of the template\.

Next, you typically create a change set and then execute it\. \(Processing macros can add multiple resources that you might not be aware of\. To ensure that you're aware of all of the changes introduced by macros, we strongly advise that you use change sets\.\) AWS CloudFormation passes the specified template content, along with any additional specified parameters, to the Lambda function specified in the macro resource\. The Lambda function returns the processed template content, be it a snippet or an entire template\. 

After all macros in the template have been called, AWS CloudFormation generates a change set that includes the processed template content\. After you review the change set, execute it to apply the changes\. 

![\[Use the Fn::Transform intrinsic function or the Transform section of the template, to pass the template contents and associated parameters to the macro's underlying Lamdba function, which returns the processed template contents.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/template-macro-use.png)

**Note**  
If you are comfortable creating or updating a stack directly from a processed template, without first reviewing the proposed changes in a change set, you can do so by specifying the `CAPABILITY_AUTO_EXPAND` capability during a `CreateStack` or `UpdateStack` request\. You should only create stacks directly from a stack template that contains macros if you know what processing the macro performs\.   
In addition, change sets do not currently support nested stacks\. If you want to create a stack from a stack template that contains macros and nested stacks, you must create the stack directly from the template using this capability\.   
For more information, see [CreateStack](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_CreateStack.html) or [UpdateStack](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_UpdateStack.html) in the *AWS CloudFormation API Reference*\.

## Creating an AWS CloudFormation macro definition<a name="template-macros-author"></a>

When you create a macro definition, the macro definition makes the underlying Lambda function available in the specified account so that AWS CloudFormation can invokes it to process the templates\.

### AWS CloudFormation macro function interface<a name="template-macros-lambda-interface"></a>

For macros, AWS CloudFormation invokes the underlying Lambda functions with the following event mapping\. AWS CloudFormation sends its request in JSON format, and it expects the function response to be formatted as JSON too\.

```
{
    "region" : "us-east-1", 
    "accountId" : "$ACCOUNT_ID", 
    "fragment" : { ... }, 
    "transformId" : "$TRANSFORM_ID", 
    "params" : { ... }, 
    "requestId" : "$REQUEST_ID",
    "templateParameterValues" : { ... } 
}
```
+ **region**

  The region in which the macro resides\.
+ **accountId**

  The account ID of the account from which the macro is invoking the Lambda function\.
+ **fragment**

  The template content available for custom processing, in JSON format\.
  + For macros included in the `Transform` template section, this is the entire template except for the `Transform` section\.
  + For macros included in an `Fn::Transform` intrinsic function call, this includes all sibling nodes \(and their children\) based on the location of the intrinsic function within the template except for the `Fn::Transform` function\. For more information, see [AWS CloudFormation macro scope](#template-macros-scope)\. 
+ **transformId**

  The name of the macro invoking this function\.
+ **params**

  For `Fn::Transform` function calls, any specified parameters for the function\. AWS CloudFormation does not evaluate these parameters before passing them to the function\.

  For macros included in the `Transform` template section, this section is empty\.
+ **requestId**

  The ID of the request invoking this function\.
+ **templateParameterValues**

  Any parameters specified in the [Parameters](parameters-section-structure.md) section of the template\. AWS CloudFormation evaluates these parameters before passing them to the function\.

AWS CloudFormation expects the underlying function to return a response in the following JSON format:

```
{
    "requestId" : "$REQUEST_ID", 
    "status" : "$STATUS", 
    "fragment" : { ... } 
}
```
+ **requestId**

  The ID of the request invoking this function\. This must match the request ID provided by AWS CloudFormation when invoking the function\.
+ **status**

  The status of the request \(case\-insensitive\)\. Should be set to "success"\. AWS CloudFormation treats any other response as a failure\.
+ **fragment**

  The processed template content for AWS CloudFormation to include in the processed template, including siblings\. AWS CloudFormation replaces the template content that is passed to the Lambda function with the template fragment it receives in the Lambda response\. 

  The processed template content must be valid JSON, and its inclusion in the processed template must result in a valid template\.

  If your function doesn't actually change the template content that AWS CloudFormation passes to it, but you still need to include that content in the processed template, your function needs to return that template content to AWS CloudFormation in its response\.
+ **errorMessage**

  The error message that explains why the transform failed\. CloudFormation displays this error message in the **Events** pane of the **Stack details** page for your stack\. 

  For example, "Error creating change set: Transform *AWS account number*::*macro name* failed with: *error message string*"\.

For information about additional considerations when creating macros, see [Considerations when creating AWS CloudFormation macro definitions](#template-macros-considerations)\.

### AWS CloudFormation macro account scope and permissions<a name="template-macros-permissions"></a>

You can use macros only in the account in which they were created as a resource\. The name of the macro must be unique within a given account\. However, you can make the same functionality available in multiple accounts by enabling cross\-account access on the underlying Lambda function, and then creating macro definitions referencing that function in multiple accounts\. In the example below, three accounts contain macro definitions that each point to the same Lambda function\. 

![\[By allowing cross-account access on the Lamdba function, AWS enables you to create macros in multiple accounts that reference that function.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/template-macro-accounts.png)

For more information, see [Overview of managing access permissions to your AWS Lambda resources](https://docs.aws.amazon.com/lambda/latest/dg/access-control-overview.html) in the *AWS Lambda Developer Guide*\.

In order to create a macro definition, the user must have permissions to create a stack within the specified account\. 

In order for AWS CloudFormation to successfully run a macro included in a template, the user must have `Invoke` permissions for the underlying Lambda function\. To prevent potential escalation of privileges, AWS CloudFormation impersonates the user while running the macro\. For more information, see [Lambda permissions model](https://docs.aws.amazon.com/lambda/latest/dg/intro-permission-model.html) in the *AWS Lambda Developer Guide* and [Actions and condition context keys for AWS Lambda](https://docs.aws.amazon.com/IAM/latest/UserGuide/list_lambda.html) in the *IAM User Guide*\.

The [AWS::Serverless transform](transform-aws-serverless.md) and [AWS::Include transform](create-reusable-transform-function-snippets-and-add-to-your-template-with-aws-include-transform.md) transforms are macros hosted by AWS CloudFormation\. No special permissions are necessary to use them, and they are available from within any account in AWS CloudFormation\.

### Debugging AWS CloudFormation macros<a name="template-macros-debug"></a>

To aid in debugging, you can also specify the `LogGroupName` and `LogRoleArn` properties when creating the [AWS::CloudFormation::Macro](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-macro.html) resource type for your macro\. These properties enable you to specify the CloudWatch log group to which AWS CloudFormation sends error logging information when invoking the macro's underlying AWS Lambda function, and the role AWS CloudFormation should assume when sending log entries to those logs\.

### Billing<a name="template-macros-billing"></a>

When a macro is run, the owner of the Lambda function is billed for any charges related to the execution of that function\.

The [AWS::Serverless transform](transform-aws-serverless.md) and [AWS::Include transform](create-reusable-transform-function-snippets-and-add-to-your-template-with-aws-include-transform.md) transforms are macros hosted by AWS CloudFormation\. There is no charge for using them\.

### Considerations when creating AWS CloudFormation macro definitions<a name="template-macros-considerations"></a>

When creating macro definitions, keep the following in mind:
+ Macros are supported only in regions where AWS Lambda is available\. For a list of regions where Lambda is available, see [http://docs.aws.amazon.com/general/latest/gr/rande.html#lambda_region](http://docs.aws.amazon.com/general/latest/gr/rande.html#lambda_region)\.
+ Any processed template snippets must be valid JSON\.
+ Any processed template snippets must pass validation checks for a create stack or update stack operation\.
+ AWS CloudFormation resolves macros first, and then processes the template\. The resulting template must be valid JSON and must not exceed the template size limit\.
+ Because of the order in which CloudFormation processes elements in a template, a macro cannot include modules in the processed template content it returns to CloudFormation\. For more information on modules, see [Developing modules](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/modules.html) in the *CloudFormation CLI User Guide*\.
+ When using the update rollback feature, AWS CloudFormation uses a copy of the original template\. It rolls back to the original template even if the included snippet was changed\.
+ Including macros within macros does not work because we do not process macros iteratively\.
+ The `Fn::ImportValue` intrinsic function isn't currently supported in macros\.
+ Intrinsic functions included in the template are evaluated after any macros\. Therefore, the processed template content your macro returns can include calls to intrinsic functions, and they are evaluated as usual\.
+ AWS CloudFormation macros are not supported in stack sets\.
+ Change sets do not currently support nested stacks\. If you want to create or update a stack using a stack template that contains macros *and* nested stacks, you must create or update the stack directly\. To do this, use the [CreateStack](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_CreateStack.html.html) or [UpdateStack](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_UpdateStack.html.html) action and specify the `CAPABILITY_AUTO_EXPAND` capability\.

**To create a AWS CloudFormation macro definition**

1. [ Build an AWS Lambda function](https://docs.aws.amazon.com/lambda/latest/dg/lambda-app.html) that processes AWS CloudFormation templates\.

   The Lambda function you build performs the processing of the template contents\. Your function can process any part of a template, up to the entire template\. For information about the event mapping to which your function must adhere, see [AWS CloudFormation macro function interface](#template-macros-lambda-interface)\. For information about additional considerations when creating macros, see [Considerations when creating AWS CloudFormation macro definitions](#template-macros-considerations)\.

1. [Create a template](template-guide.md) containing a [AWS::CloudFormation::Macro](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-macro.html) resource type\.
   + You must specify the `Name` and `FunctionName` properties\. The `FunctionName` property specifies the ARN of the Lambda function to invoke when AWS CloudFormation runs the macro\.
   + To aid in debugging, you can also specify the `LogGroupName` and `LogRoleArn` properties\. 

1. [Create a stack](cfn-console-create-stack.md) from the template containing the macro in the desired account\.

   After AWS CloudFormation has successfully created the stack that contains the macro definition, the macro is available for use within that account\.

## Using AWS CloudFormation macros in your templates<a name="template-macros-use"></a>

After AWS CloudFormation has successfully created the stack which contains the macro definition, the macro is available for use within that account\. You use a macro by referencing it in the stack template, at the appropriate location relevant to the template contents you want to process\.

### AWS CloudFormation macro evaluation order<a name="template-macros-order"></a>

 You can reference multiple macros in a given template, including transforms hosted by AWS CloudFormation, such as [AWS::Include transform](create-reusable-transform-function-snippets-and-add-to-your-template-with-aws-include-transform.md) and [AWS::Serverless transform](transform-aws-serverless.md)\. 

Macros are evaluated in order, based on their location in the template, from the most deeply nested outward to the most general\. Macros at the same location in the template are evaluated serially based on the order in which they are listed\. 

Transforms such as `AWS::Include` and `AWS::Transform` are treated the same as any other macros in terms of action order and scope\.

For example, in the template sample below, AWS CloudFormation evaluates the `PolicyAdder` macro first, because it is the most deeply\-nested macro in the template\. AWS CloudFormation then evaluates `MyMacro` before evaluating `AWS::Serverless` because it is listed before `AWS::Serverless` in the `Transform` section\.

```
AWSTemplateFormatVersion: 2010-09-09 
 Transform: [MyMacro, AWS::Serverless]
 Resources:
    WaitCondition:
      Type: AWS::CloudFormation::WaitCondition
    MyBucket:
      Type: 'AWS::S3::Bucket'  
      Properties:
        BucketName: MyBucket 
        Tags: [{"key":"value"}] 
        'Fn::Transform':
          - Name: PolicyAdder
        CorsConfiguration:[]   
    MyEc2Instance:
      Type: 'AWS::EC2::Instance' 
      Properties:
        ImageID: "ami-123"
```

### AWS CloudFormation macro scope<a name="template-macros-scope"></a>

Macros referenced in the `Transform` section of a template can process the entire contents of that template\.

Macros referenced in a `Fn::Transform` function can process the contents of any of the sibling elements \(including children\) of that `Fn::Transform` function in the template\.

For example, in the template sample below, `AWS::Include` can process all of the `MyBucket` properties, based on the location of the `Fn::Transform` function that contains it\. `MyMacro` can process the contents of the entire template because of its inclusion in the `Transform` section\.

```
// Start of processable content for MyMacro
AWSTemplateFormatVersion: 2010-09-09 
 Transform: [MyMacro]
 Resources:
    WaitCondition:
      Type: AWS::CloudFormation::WaitCondition
    MyBucket:
      Type: 'AWS::S3::Bucket'  //Start of processable content for AWS::Include
      Properties:
        BucketName: MyBucket 
        Tags: [{"key":"value"}] 
        'Fn::Transform':
          - Name: 'AWS::Include'
              Parameters:
                Location: s3://MyAmazonS3BucketName/MyFileName.yaml
        CorsConfiguration:[]   //End of processable content for AWS::Include
    MyEc2Instance:
      Type: 'AWS::EC2::Instance' 
      Properties:
        ImageID: "ami-123"
// End of processable content for MyMacro
```

### Change sets and AWS CloudFormation macros<a name="template-macros-change-sets"></a>

To create or update a stack using a template that references macros, you typically create a change set and then execute it\. A change set describes the actions CloudFormation will take based on the processed template\. Processing macros can add multiple resources that you might not be aware of\. To ensure that you're aware of all of the changes introduced by macros, we strongly recommend you use change sets\. After you review the change set, you can execute it to actually apply the changes\.

A macro can add IAM resources to your template\. For these resources, AWS CloudFormation requires you to [acknowledge their capabilities](using-iam-template.md#using-iam-capabilities)\. Because AWS CloudFormation can't know which resources are added before processing your template, you might need to acknowledge IAM capabilities when you create the change set, depending on whether the referenced macros contain IAM resources\. That way, when you run the change set, AWS CloudFormation has the necessary capabilities to create IAM resources\.

**Note**  
If you are comfortable creating or updating a stack directly from a processed template, without first reviewing the proposed changes in a change set, you can do so by specifying the `CAPABILITY_AUTO_EXPAND` capability during a `CreateStack` or `UpdateStack` request\. You should only create stacks directly from a stack template that contains macros if you know what processing the macro performs\.   
In addition, change sets do not currently support nested stacks\. If you want to create a stack from a stack template that contains macros and nested stacks, you must create the stack directly from the template using this capability\.   
For more information, see [CreateStack](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_CreateStack.html) or [UpdateStack](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_UpdateStack.html) in the *AWS CloudFormation API Reference*\.

If you use the AWS CLI, you can use the `package` and `deploy` commands to reduce the number of steps for launching stacks from templates that reference macros\. For more information, see [Deploying Lambda\-based applications](https://docs.aws.amazon.com/lambda/latest/dg/deploying-lambda-apps.html) in the *AWS Lambda Developer Guide*\.

### Template stage and CloudFormation macros<a name="template-macros-template-stage"></a>

A template's *stage* indicates whether the template is the original user\-submitted template or one in which AWS CloudFormation has processed the macros\.
+ `Original`: The template that the user originally submitted to create or update the stack\. 
+ `Processed`: The template AWS CloudFormation used to create or update the stack after processing any referenced macros\. The processed template is formatted as JSON, even if the original template was formatted as YAML\.

Use the processed template for troubleshooting stack issues\. If a template doesn't reference macros, the original and processed templates are identical\.

You can use the AWS CloudFormation [console](cfn-console-view-stack-data-resources.md) or [AWS CLI](using-cfn-get-template.md) to see the stage of a stack template\.

**Note**  
The maximum size for a processed stack template is 51,200 bytes when passed directly into a `CreateStack`, `UpdateStack`, or `ValidateTemplate` request, or 460,800 bytes when passed as an S3 object using an Amazon S3 template URL\. However, during processing CloudFormation updates the temporary state of the template as it serially processes the macros contained in the template\. Because of this, the size of the template *during processing* may temporarily exceed the allowed size of a fully\-processed template\. CloudFormation allows some buffer for these in\-process templates\. However, you should design your templates and macros keeping in mind the maximum allowed size for a processed stack template\.  
If CloudFormation returns a `Transformation data limit exceeded` error while processing your template, your template has exceeded the maximum template size CloudFormation allows during processing\.   
To resolve this issue, consider doing the following:  
Restructure your template into multiple templates to avoid exceeding the maximum size for in\-process templates\. For example:  
Use nested stack templates to encapsulate parts of the template\. For more information, see [Working with nested stacks](using-cfn-nested-stacks.md)\.
Create multiple stacks and use cross\-stack references to exchange information between them\. For more information, see [Walkthrough: Refer to resource outputs in another AWS CloudFormation stack](walkthrough-crossstackref.md)\.
Reduce the size of template fragment returned by a given macro\. CloudFormation does not tamper with the contents of fragments returned by macros\.

**To use a AWS CloudFormation macro in your template**
**Note**  
In order for AWS CloudFormation to successfully run a macro referenced in a template, the user must have `Invoke` permissions for the underlying Lambda function\. For more information, see [Overview of managing access permissions to your AWS Lambda resources](https://docs.aws.amazon.com/lambda/latest/dg/access-control-overview.html) in the *AWS Lambda Developer Guide*\.

1. Include a reference to the macro in the template\.
   + To process a template snippet, reference the macro in a ``Fn::Transform`` function located relative to the template content you want to process\.
   + To process the entire template, reference the macro in the [Transform](transform-section-structure.md) section of the template\.

1. [Create a change set](using-cfn-updating-stacks-changesets-create.md) using the template\.

1. Review and [run the change set](using-cfn-updating-stacks-changesets-execute.md)\.

## Macro examples<a name="template-macros-examples-list"></a>

In addition to the [Macro example: Creating and using a macro](macros-example.md) walkthrough in this guide, you can find example macros, including source code and templates, in the [Macros examples](https://github.com/awslabs/aws-cloudformation-templates/tree/master/aws/services/CloudFormation/MacrosExamples/) section of the [Amazon Web Services \- Labs](https://github.com/awslabs) repo on GitHub\. These examples are provided 'as\-is' for instructional purposes\. 

## See also<a name="template-macros-seealso"></a>

[AWS::CloudFormation::Macro](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-macro.html)

[Transform](transform-section-structure.md)

[`Fn::Transform`](intrinsic-function-reference-transform.md)

[AWS::Serverless transform](transform-aws-serverless.md)

[AWS::Include transform](create-reusable-transform-function-snippets-and-add-to-your-template-with-aws-include-transform.md)