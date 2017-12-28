# AWS::CloudFormation::Stack<a name="aws-properties-stack"></a>

The `AWS::CloudFormation::Stack` type nests a stack as a resource in a top\-level template\.

You can add output values from a nested stack within the containing template\. You use the GetAtt function with the nested stack's logical name and the name of the output value in the nested stack in the format `Outputs.NestedStackOutputName`\.

**Important**  
We strongly recommend that updates to nested stacks are run from the parent stack\.

When you apply template changes to update a top\-level stack, AWS CloudFormation updates the top\-level stack and initiates an update to its nested stacks\. AWS CloudFormation updates the resources of modified nested stacks, but does not update the resources of unmodified nested stacks\. For more information, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.

**Note**  
You must acknowledge IAM capabilities for nested stacks that contain IAM resources\. Also, verify that you have cancel update stack permissions, which is required if an update rolls back\. For more information about IAM and AWS CloudFormation, see [Controlling Access with AWS Identity and Access Management](using-iam-template.md)\.


+ [Syntax](#aws-resource-cloudformation-stack-syntax)
+ [Properties](#aws-properties-stack-prop)
+ [Return Values](#w3ab2c21c10d170c19)
+ [Related Information](#w3ab2c21c10d170c21)

## Syntax<a name="aws-resource-cloudformation-stack-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-stack-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::Stack",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudformation-stack-notificationarns)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudformation-stack-parameters)" : { [AWS CloudFormation Stack Parameters](aws-properties-stack-parameters.md) },
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudformation-stack-tags)" : [ Resource Tag, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudformation-stack-templateurl)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudformation-stack-timeoutinminutes)" : Integer
  }
}
```

### YAML<a name="aws-resource-cloudformation-stack-syntax.yaml"></a>

```
Type: "AWS::CloudFormation::Stack"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudformation-stack-notificationarns):
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudformation-stack-parameters):
    [AWS CloudFormation Stack Parameters](aws-properties-stack-parameters.md)
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudformation-stack-tags):
    - Resource Tag
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudformation-stack-templateurl): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudformation-stack-timeoutinminutes): Integer
```

## Properties<a name="aws-properties-stack-prop"></a>

`NotificationARNs`  
A list of existing Amazon SNS topics where notifications about stack events are sent\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`Parameters`  
The set of parameters passed to AWS CloudFormation when this nested stack is created\.  
If you use the `Ref` function to pass a parameter value to a nested stack, comma\-delimited list parameters must be of type `String`\. In other words, you cannot pass values that are of type `CommaDelimitedList` to nested stacks\.
*Required*: Conditional \(required if the nested stack requires input parameters\)\.  
*Type*: [AWS CloudFormation Stack Parameters](aws-properties-stack-parameters.md)  
*Update requires*: Whether an update causes interruptions depends on the resources that are being updated\. An update never causes a nested stack to be replaced\.

`Tags`  
An arbitrary set of tags \(key–value pairs\) to describe this stack\.  
*Required: *No  
*Type*:   
*Update requires*: No interruption\.

`TemplateURL`  
The URL of a template that specifies the stack that you want to create as a resource\. Template files can use any extension, such as `.json`, `.yaml`, `.template`, or `.txt`\. The template must be stored on an Amazon S3 bucket, so the URL must have the form: `https://s3.amazonaws.com/.../TemplateName.extension`  
*Required: *Yes  
*Type*: String  
*Update requires*: Whether an update causes interruptions depends on the resources that are being updated\. An update never causes a nested stack to be replaced\.

`TimeoutInMinutes`  
The length of time, in minutes, that AWS CloudFormation waits for the nested stack to reach the `CREATE_COMPLETE` state\. The default is no timeout\. When AWS CloudFormation detects that the nested stack has reached the `CREATE_COMPLETE` state, it marks the nested stack resource as `CREATE_COMPLETE` in the parent stack and resumes creating the parent stack\. If the timeout period expires before the nested stack reaches `CREATE_COMPLETE`, AWS CloudFormation marks the nested stack as failed and rolls back both the nested stack and parent stack\.  
*Required: *No  
*Type*: Integer  
*Update requires*: Updates are not supported\.

## Return Values<a name="w3ab2c21c10d170c19"></a>

### Ref<a name="w3ab2c21c10d170c19b2"></a>

For `AWS::CloudFormation::Stack`, `Ref` returns the Stack ID\. For example:

`arn:aws:cloudformation:``us-east-2``:123456789012:stack/mystack-mynestedstack-sggfrhxhum7w/f449b250-b969-11e0-a185-5081d0136786`

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d170c19b4"></a>

`Outputs.NestedStackOutputName`  
*Returns*: The output value from the specified nested stack where *NestedStackOutputName* is the name of the output value\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Related Information<a name="w3ab2c21c10d170c21"></a>

+ For sample template snippets, see Nested Stacks in [AWS CloudFormation Template Snippets](quickref-cloudformation.md)\.

+ If you have nested stacks that are stuck in an in\-progress operation, see Troubleshooting Errors in [Troubleshooting AWS CloudFormation](troubleshooting.md)\.