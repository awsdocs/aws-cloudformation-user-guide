# AWS::SSM::Parameter<a name="aws-resource-ssm-parameter"></a>

The `AWS::SSM::Parameter` resource creates an SSM parameter in AWS Systems Manager Parameter Store\.

**Important**  
To create an SSM parameter, you must have the AWS Identity and Access Management \(IAM\) permissions `ssm:PutParameter` and `ssm:AddTagsToResource`\. On stack creation, AWS CloudFormation adds the following three tags to the parameter: `aws:cloudformation:stack-name`, `aws:cloudformation:logical-id`, and `aws:cloudformation:stack-id`, in addition to any custom tags you specify\.  
To add, update, or remove tags during stack update, you must have IAM permissions for both `ssm:AddTagsToResource` and `ssm:RemoveTagsFromResource`\. For more information, see [AWS Systems Manager Permissions Reference](https://docs.aws.amazon.com/systems-manager/latest/userguide/auth-and-access-control-permissions-reference.html) in the *AWS Systems Manager User Guide*\.

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
      "[Policies](#cfn-ssm-parameter-policies)" : String,
      "[Tags](#cfn-ssm-parameter-tags)" : Json,
      "[Tier](#cfn-ssm-parameter-tier)" : String,
      "[Type](#cfn-ssm-parameter-type)" : String,
      "[Value](#cfn-ssm-parameter-value)" : String
    }
}
```

### YAML<a name="aws-resource-ssm-parameter-syntax.yaml"></a>

```
Type: AWS::SSM::Parameter
Properties: 
  [AllowedPattern](#cfn-ssm-parameter-allowedpattern): String
  [Description](#cfn-ssm-parameter-description): String
  [Name](#cfn-ssm-parameter-name): String
  [Policies](#cfn-ssm-parameter-policies): String
  [Tags](#cfn-ssm-parameter-tags): Json
  [Tier](#cfn-ssm-parameter-tier): String
  [Type](#cfn-ssm-parameter-type): String
  [Value](#cfn-ssm-parameter-value): String
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

`Policies`  <a name="cfn-ssm-parameter-policies"></a>
Information about the policies assigned to a parameter\.  
 [Working with Parameter Policies](https://docs.aws.amazon.com/systems-manager/latest/userguide/parameter-store-policies.html) in the *AWS Systems Manager User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ssm-parameter-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tier`  <a name="cfn-ssm-parameter-tier"></a>
The parameter tier\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `Advanced | Standard`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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

The following example snippet creates a Systems Manager parameter with a `String` type and adds the tag key\-value pair `"Environment":"Dev"`\.

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
            "AllowedPattern" : "^[a-zA-Z]{1,10}$",
            "Tags": {
               "Environment": "DEV"
            }
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
      Tags:
        "Environment": "DEV"
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

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
