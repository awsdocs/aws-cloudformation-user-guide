# AWS::SSM::Parameter<a name="aws-resource-ssm-parameter"></a>

The `AWS::SSM::Parameter` resource creates an Amazon EC2 Systems Manager \(SSM\) parameter in Parameter Store\.


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
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-parameter-name)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-parameter-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-parameter-type)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-parameter-value)" : String
  }
}
```

### YAML<a name="aws-resource-ssm-parameter-syntax.yaml"></a>

```
Type: "AWS::SSM::Parameter"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-parameter-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-parameter-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-parameter-type): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-parameter-value): String
```

## Properties<a name="aws-resource-ssm-parameter-properties"></a>

`Name`  
The name of the parameter\. Names must not be prefixed with `aws` or `ssm`\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Description`  
Information about the parameter that you want to add to the system\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`Type`  
The type of parameter\. Valid values include the following: `String` or `StringList`\.  
AWS CloudFormation doesn't support the `SecureString` parameter type\.
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`Value`  
The parameter value\. Value must not nest another parameter\. Do not use `{{}}` in the value\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

## Return Value<a name="aws-resource-ssm-parameter-returnvalues"></a>

### Ref<a name="w3ab2c21c10e1021c11b2"></a>

When you pass the logical ID of an `AWS::SSM::Parameter` resource to the intrinsic `Ref` function, the function returns the Name of the SSM parameter\. For example, `ssm-myparameter-ABCNPH3XCAO6`\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10e1021c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Type`  
Returns the type of the parameter\. Valid values are `String` or `StringList`\.

`Value`  
Returns the value of the parameter\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Examples<a name="aws-resource-ssm-parameter-examples"></a>

### SSM Parameter \(String\) Example<a name="w3ab2c21c10e1021c13b2"></a>

The following example snippet creates an SSM parameter in the Parameter Store\.

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
            "Description": "SSM Parameter for running date command."
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
```

### SSM Parameter \(StringList\) Example<a name="w3ab2c21c10e1021c13b4"></a>

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
            "Description": "SSM Parameter of type StringList."
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
```