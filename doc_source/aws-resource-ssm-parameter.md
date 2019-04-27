# AWS::SSM::Parameter<a name="aws-resource-ssm-parameter"></a>

The `AWS::SSM::Parameter` resource creates an SSM parameter in AWS Systems Manager Parameter Store\.

For information about valid values for parameters, see [Requirements and Constraints for Parameter Names](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-parameter-name-constraints.html) in the *AWS Systems Manager User Guide* and [PutParameter](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_PutParameter.html) in the *AWS Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-parameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-parameter-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::Parameter",
  "Properties" : {
      "[AllowedPattern](#cfn-ssm-parameter-allowedpattern)" : String,
      "[Description](#cfn-ssm-parameter-description)" : String,
      "[Name](#cfn-ssm-parameter-name)" : String,
      "[Type](#cfn-ssm-parameter-type)" : String,
      "[Value](#cfn-ssm-parameter-value)" : String
    }
}
```

### YAML<a name="aws-resource-ssm-parameter-syntax.yaml"></a>

```
Type: AWS::SSM::Parameter
Properties : 
﻿  [AllowedPattern](#cfn-ssm-parameter-allowedpattern) : String
﻿  [Description](#cfn-ssm-parameter-description) : String
﻿  [Name](#cfn-ssm-parameter-name) : String
﻿  [Type](#cfn-ssm-parameter-type) : String
﻿  [Value](#cfn-ssm-parameter-value) : String
```

## Properties<a name="aws-resource-ssm-parameter-properties"></a>

`AllowedPattern`  <a name="cfn-ssm-parameter-allowedpattern"></a>
A regular expression used to validate the parameter value\. For example, for String types with values restricted to numbers, you can specify the following: `AllowedPattern=^\d+$`   
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-ssm-parameter-description"></a>
Information about the parameter\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ssm-parameter-name"></a>
The name of the parameter\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-ssm-parameter-type"></a>
The type of parameter\. Valid values include the following: `String` or `StringList`\.  
AWS CloudFormation doesn't support the `SecureString` parameter type\.
*Required*: Yes  
*Type*: String  
*Allowed Values*: `SecureString | String | StringList`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-ssm-parameter-value"></a>
The parameter value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-ssm-parameter-return-values"></a>

### Ref<a name="aws-resource-ssm-parameter-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Name of the SSM parameter\. For example, `ssm-myparameter-ABCNPH3XCAO6`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ssm-parameter-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ssm-parameter-return-values-fn--getatt-fn--getatt"></a>

`Type`  <a name="Type-fn::getatt"></a>
Returns the type of the parameter\. Valid values are `String` or `StringList`\.

`Value`  <a name="Value-fn::getatt"></a>
Returns the value of the parameter\.

## Examples<a name="aws-resource-ssm-parameter--examples"></a>

### AWS Systems Manager Parameter String Example<a name="aws-resource-ssm-parameter--examples--AWS_Systems_Manager_Parameter_String_Example"></a>

The following example snippet creates a Systems Manager parameter with a `String` type\.

#### JSON<a name="aws-resource-ssm-parameter--examples--AWS_Systems_Manager_Parameter_String_Example--json"></a>

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

#### YAML<a name="aws-resource-ssm-parameter--examples--AWS_Systems_Manager_Parameter_String_Example--yaml"></a>

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

### AWS Systems Manager Parameter StringList Example<a name="aws-resource-ssm-parameter--examples--AWS_Systems_Manager_Parameter_StringList_Example"></a>

The following example creates a Systems Manager parameter with a `StringList` type\.

#### JSON<a name="aws-resource-ssm-parameter--examples--AWS_Systems_Manager_Parameter_StringList_Example--json"></a>

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

#### YAML<a name="aws-resource-ssm-parameter--examples--AWS_Systems_Manager_Parameter_StringList_Example--yaml"></a>

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