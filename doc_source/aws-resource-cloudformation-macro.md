# AWS::CloudFormation::Macro<a name="aws-resource-cloudformation-macro"></a>

The `AWS::CloudFormation::Macro` resource is an CloudFormation resource type that creates an CloudFormation macro to perform custom processing on CloudFormation templates\. For more information, see [Using AWS CloudFormation macros to perform custom processing on templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-macros.html)\.

## Syntax<a name="aws-resource-cloudformation-macro-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-macro-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::Macro",
  "Properties" : {
      "[Description](#cfn-cloudformation-macro-description)" : String,
      "[FunctionName](#cfn-cloudformation-macro-functionname)" : String,
      "[LogGroupName](#cfn-cloudformation-macro-loggroupname)" : String,
      "[LogRoleARN](#cfn-cloudformation-macro-logrolearn)" : String,
      "[Name](#cfn-cloudformation-macro-name)" : String
    }
}
```

### YAML<a name="aws-resource-cloudformation-macro-syntax.yaml"></a>

```
Type: AWS::CloudFormation::Macro
Properties: 
  [Description](#cfn-cloudformation-macro-description): String
  [FunctionName](#cfn-cloudformation-macro-functionname): String
  [LogGroupName](#cfn-cloudformation-macro-loggroupname): String
  [LogRoleARN](#cfn-cloudformation-macro-logrolearn): String
  [Name](#cfn-cloudformation-macro-name): String
```

## Properties<a name="aws-resource-cloudformation-macro-properties"></a>

`Description`  <a name="cfn-cloudformation-macro-description"></a>
A description of the macro\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FunctionName`  <a name="cfn-cloudformation-macro-functionname"></a>
The Amazon Resource Name \(ARN\) of the underlying AWS Lambda function that you want AWS CloudFormation to invoke when the macro is run\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogGroupName`  <a name="cfn-cloudformation-macro-loggroupname"></a>
The Amazon CloudWatch log group to which AWS CloudFormation sends error logging information when invoking the macro's underlying AWS Lambda function\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogRoleARN`  <a name="cfn-cloudformation-macro-logrolearn"></a>
The ARN of the role AWS CloudFormation should assume when sending log entries to CloudWatch logs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudformation-macro-name"></a>
The name of the macro\. The name of the macro must be unique across all macros in the account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cloudformation-macro-return-values"></a>

### Ref<a name="aws-resource-cloudformation-macro-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myMacro" }` 

For the macro `myMacro`, `Ref` returns the name of the macro\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-cloudformation-macro--seealso"></a>
+  [Using AWS CloudFormation macros to perform custom processing on templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-macros.html) 