# AWS::SSM::Parameter<a name="aws-resource-ssm-parameter"></a>

The `AWS::SSM::Parameter` resource creates an SSM parameter in AWS Systems Manager Parameter Store\.

**Topics**
+ [Syntax](#aws-resource-ssm-parameter-syntax)
+ [Properties](#aws-resource-ssm-parameter-properties)
+ [Return Value](#aws-resource-ssm-parameter-returnvalues)
+ [Examples](#aws-resource-ssm-parameter-examples)

## Syntax<a name="aws-resource-ssm-parameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-parameter-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::Parameter",
  "Properties" : {
    "[Name](#cfn-ssm-parameter-name)" : String,
    "[Description](#cfn-ssm-parameter-description)" : String,
    "[Type](#cfn-ssm-parameter-type)" : String,
    "[Value](#cfn-ssm-parameter-value)" : String,
    "[AllowedPattern](#cfn-ssm-parameter-allowedpattern)" : String
  }
}
```

### YAML<a name="aws-resource-ssm-parameter-syntax.yaml"></a>

```
Type: "AWS::SSM::Parameter"
Properties: 
  [Name](#cfn-ssm-parameter-name): String
  [Description](#cfn-ssm-parameter-description): String
  [Type](#cfn-ssm-parameter-type): String
  [Value](#cfn-ssm-parameter-value): String
  [AllowedPattern](#cfn-ssm-parameter-allowedpattern): String
```

## Properties<a name="aws-resource-ssm-parameter-properties"></a>

`Name`  <a name="cfn-ssm-parameter-name"></a>
The name of the parameter\. Names must not be prefixed with `aws` or `ssm`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Description`  <a name="cfn-ssm-parameter-description"></a>
Information about the parameter that you want to add to the system\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Type`  <a name="cfn-ssm-parameter-type"></a>
The type of parameter\. Valid values include the following: `String` or `StringList`\.  
AWS CloudFormation doesn't support the `SecureString` parameter type\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Value`  <a name="cfn-ssm-parameter-value"></a>
The parameter value\. Value must not nest another parameter\. Do not use `{{}}` in the value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AllowedPattern`  <a name="cfn-ssm-parameter-allowedpattern"></a>
A regular expression used to validate the parameter value\. For example, for String types with values restricted to numbers, you can specify the following: `AllowedPattern=^\d+$`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="aws-resource-ssm-parameter-returnvalues"></a>

### Ref<a name="w3ab2c21c10e1165c11b3"></a>

When you pass the logical ID of an `AWS::SSM::Parameter` resource to the intrinsic `Ref` function, the function returns the Name of the SSM parameter\. For example, `ssm-myparameter-ABCNPH3XCAO6`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10e1165c11b5"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Type`  
Returns the type of the parameter\. Valid values are `String` or `StringList`\.

`Value`  
Returns the value of the parameter\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="aws-resource-ssm-parameter-examples"></a>

### SSM Parameter \(String\) Example<a name="w3ab2c21c10e1165c13b3"></a>

The following example snippet creates an SSM parameter in Parameter Store\.

#### JSON<a name="aws-resource-ssm-parameter-example.json"></a>

```
{
   "Description": "Create SSM Parameter",
   "Resources": {
      "BasicParameter": {
         "Type": "AWS::SSM::Parameter",
         "Properties": {
            "Name": "command",
            "Type": "String",
            "Value": "date",
            "Description": "SSM Parameter for running date command.",
            "AllowedPattern" : "^[a-zA-Z]{1,10}$"
         }
      }
   }
}
```

#### YAML<a name="aws-resource-ssm-parameter-example.yaml"></a>

```
Description: "Create SSM Parameter"
Resources:
  BasicParameter:
    Type: "AWS::SSM::Parameter"
    Properties:
      Name: "command"
      Type: "String"
      Value: "date"
      Description: "SSM Parameter for running date command."
      AllowedPattern: "^[a-zA-Z]{1,10}$"
```

### SSM Parameter \(StringList\) Example<a name="w3ab2c21c10e1165c13b5"></a>

The following example creates an SSM parameter with a `StringList` type\.

#### JSON<a name="aws-resource-ssm-parameter-example2.json"></a>

```
{
   "Description": "Create SSM Parameter",
   "Resources": {
      "BasicParameter": {
         "Type": "AWS::SSM::Parameter",
         "Properties": {
            "Name": "commands",
            "Type": "StringList",
            "Value": "date,ls",
            "Description": "SSM Parameter of type StringList.",
            "AllowedPattern" : "^[a-zA-Z]{1,10}$"
         }
      }
   }
}
```

#### YAML<a name="aws-resource-ssm-parameter-example2.yaml"></a>

```
Description: "Create SSM Parameter"
Resources:
  BasicParameter:
    Type: "AWS::SSM::Parameter"
    Properties:
      Name: "commands"
      Type: "StringList"
      Value: "date,ls"
      Description: "SSM Parameter of type StringList."
      AllowedPattern: "^[a-zA-Z]{1,10}$"
```