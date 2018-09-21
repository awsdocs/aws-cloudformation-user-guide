# AWS::CloudFormation::Macro<a name="aws-resource-cloudformation-macro"></a>

The `AWS::CloudFormation::Macro` resource is an AWS CloudFormation resource type that creates an AWS CloudFormation macro to perform custom processing on AWS CloudFormation templates\. For more information, see [Using AWS CloudFormation Macros to Perform Custom Processing on Templates](template-macros.md)\. 

**Topics**
+ [Syntax](#aws-resource-cloudformation-macro-syntax)
+ [Properties](#aws-resource-cloudformation-macro-properties)
+ [Return Values](#aws-resource-cloudformation-macro-returnvalues)
+ [See Also](#aws-resource-cloudformation-macro-seealso)

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
Type: "AWS::CloudFormation::Macro"
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
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`FunctionName`  <a name="cfn-cloudformation-macro-functionname"></a>
The Amazon Resource Name \(ARN\) of the underlying AWS Lambda function that you want AWS CloudFormation to invoke when the macro is run\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LogGroupName`  <a name="cfn-cloudformation-macro-loggroupname"></a>
The Amazon CloudWatch log group to which AWS CloudFormation sends error logging information when invoking the macro's underlying AWS Lambda function\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LogRoleARN`  <a name="cfn-cloudformation-macro-logrolearn"></a>
The ARN of the role AWS CloudFormation should assume when sending log entries to CloudWatch logs\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-cloudformation-macro-name"></a>
The name of the macro\. The name of the macro must be unique across all macros in the account\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-cloudformation-macro-returnvalues"></a>

### Ref<a name="aws-resource-cloudformation-macro-ref"></a>

When you pass the logical ID of an `AWS::CloudFormation::Macro` resource to the intrinsic `Ref` function, the function returns the macro name, such as `Include` or `Serverless`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## See Also<a name="aws-resource-cloudformation-macro-seealso"></a>
+ [Using AWS CloudFormation Macros to Perform Custom Processing on Templates](template-macros.md)