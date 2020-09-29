# AWS::SSM::Parameter<a name="aws-resource-ssm-parameter"></a>

The `AWS::SSM::Parameter` resource creates an SSM parameter in AWS Systems Manager Parameter Store\.

**Important**  
To create an SSM parameter, you must have the AWS Identity and Access Management \(IAM\) permissions `ssm:PutParameter` and `ssm:AddTagsToResource`\. On stack creation, AWS CloudFormation adds the following three tags to the parameter: `aws:cloudformation:stack-name`, `aws:cloudformation:logical-id`, and `aws:cloudformation:stack-id`, in addition to any custom tags you specify\.  
To add, update, or remove tags during stack update, you must have IAM permissions for both `ssm:AddTagsToResource` and `ssm:RemoveTagsFromResource`\. For more information, see [Managing Access Using Policies](https://docs.aws.amazon.com/systems-manager/latest/userguide/security-iam.html#security_iam_access-manage) in the *AWS Systems Manager User Guide*\.

For information about valid values for parameters, see [Requirements and Constraints for Parameter Names](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-parameter-name-constraints.html) in the *AWS Systems Manager User Guide* and [PutParameter](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_PutParameter.html) in the *AWS Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-parameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-parameter-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::Parameter",
  "Properties" : {
      "[AllowedPattern](#cfn-ssm-parameter-allowedpattern)" : String,
      "[DataType](#cfn-ssm-parameter-datatype)" : String,
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
  [DataType](#cfn-ssm-parameter-datatype): String
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

`DataType`  <a name="cfn-ssm-parameter-datatype"></a>
The data type of the parameter, such as `text` or `aws:ec2:image`\. The default is `text`\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
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
 [Assigning parameter policies](https://docs.aws.amazon.com/systems-manager/latest/userguide/parameter-store-policies.html) in the *AWS Systems Manager User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ssm-parameter-tags"></a>
Optional metadata that you assign to a resource in the form of an arbitrary set of tags \(key\-value pairs\)\. Tags enable you to categorize a resource in different ways, such as by purpose, owner, or environment\. For example, you might want to tag a Systems Manager parameter to identify the type of resource to which it applies, the environment, or the type of configuration data referenced by the parameter\.  
*Required*: No  
*Type*: Json  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tier`  <a name="cfn-ssm-parameter-tier"></a>
The parameter tier\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Advanced | Intelligent-Tiering | Standard`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-ssm-parameter-type"></a>
The type of parameter\.  
AWS CloudFormation doesn't support creating a `SecureString` parameter type\.
*Allowed Values*: String \| StringList  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-ssm-parameter-value"></a>
The parameter value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ssm-parameter-return-values"></a>

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

### Create a String\-type parameter<a name="aws-resource-ssm-parameter--examples--Create_a_String-type_parameter"></a>

The following example creates a Systems Manager parameter named command with a `String` type and adds the tag key\-value pair `"Environment":"Dev"`\.

#### JSON<a name="aws-resource-ssm-parameter--examples--Create_a_String-type_parameter--json"></a>

```
{
    "Resources": {
        "BasicParameter": {
            "Type": "AWS::SSM::Parameter",
            "Properties": {
                "Name": "command",
                "Type": "String",
                "Value": "date",
                "Description": "SSM Parameter for running date command.",
                "AllowedPattern": "^[a-zA-Z]{1,10}$",
                "Tags": {
                    "Environment": "DEV"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-parameter--examples--Create_a_String-type_parameter--yaml"></a>

```
---
Resources:
  BasicParameter:
    Type: AWS::SSM::Parameter
    Properties:
      Name: command
      Type: String
      Value: date
      Description: SSM Parameter for running date command.
      AllowedPattern: "^[a-zA-Z]{1,10}$"
      Tags:
        Environment: DEV
```

### Create a StringList\-type parameter<a name="aws-resource-ssm-parameter--examples--Create_a_StringList-type_parameter"></a>

The following example creates a Systems Manager parameter named commands with a `StringList` type\.

#### JSON<a name="aws-resource-ssm-parameter--examples--Create_a_StringList-type_parameter--json"></a>

```
{
    "Resources": {
        "BasicParameter": {
            "Type": "AWS::SSM::Parameter",
            "Properties": {
                "Name": "commands",
                "Type": "StringList",
                "Value": "date,ls",
                "Description": "SSM Parameter of type StringList.",
                "AllowedPattern": "^[a-zA-Z]{1,10}$"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-parameter--examples--Create_a_StringList-type_parameter--yaml"></a>

```
---
Resources:
  BasicParameter:
    Type: AWS::SSM::Parameter
    Properties:
      Name: commands
      Type: StringList
      Value: date,ls
      Description: SSM Parameter of type StringList.
      AllowedPattern: "^[a-zA-Z]{1,10}$"
```

### Create an advanced tier parameter and assign a policy<a name="aws-resource-ssm-parameter--examples--Create_an_advanced_tier_parameter_and_assign_a_policy"></a>

The following example creates a Systems Manager advanced tier parameter named command with a `String` type and a parameter policy\.

#### JSON<a name="aws-resource-ssm-parameter--examples--Create_an_advanced_tier_parameter_and_assign_a_policy--json"></a>

```
{
    "Resources": {
        "BasicParameter": {
            "Type": "AWS::SSM::Parameter",
            "Properties": {
                "Name": "command",
                "Type": "String",
                "Value": "date",
                "Tier": "Advanced",
                "Policies": "[{\"Type\":\"Expiration\",\"Version\":\"1.0\",\"Attributes\":{\"Timestamp\":\"2020-05-13T00:00:00.000Z\"}},{\"Type\":\"ExpirationNotification\",\"Version\":\"1.0\",\"Attributes\":{\"Before\":\"5\",\"Unit\":\"Days\"}},{\"Type\":\"NoChangeNotification\",\"Version\":\"1.0\",\"Attributes\":{\"After\":\"60\",\"Unit\":\"Days\"}}]",
                "Description": "SSM Parameter for running date command.",
                "AllowedPattern": "^[a-zA-Z]{1,10}$",
                "Tags": {
                    "Environment": "DEV"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-parameter--examples--Create_an_advanced_tier_parameter_and_assign_a_policy--yaml"></a>

```
---
Resources:
  BasicParameter:
    Type: AWS::SSM::Parameter
    Properties:
      Name: command
      Type: String
      Value: date
      Tier: Advanced
      Policies: '[{"Type":"Expiration","Version":"1.0","Attributes":{"Timestamp":"2020-05-13T00:00:00.000Z"}},{"Type":"ExpirationNotification","Version":"1.0","Attributes":{"Before":"5","Unit":"Days"}},{"Type":"NoChangeNotification","Version":"1.0","Attributes":{"After":"60","Unit":"Days"}}]'
      Description: SSM Parameter for running date command.
      AllowedPattern: "^[a-zA-Z]{1,10}$"
      Tags:
        Environment: DEV
```

## See also<a name="aws-resource-ssm-parameter--seealso"></a>
+  [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html) 
+  [About Advanced Parameters](https://docs.aws.amazon.com/systems-manager/latest/userguide/parameter-store-advanced-parameters.html)
+  [Working with Parameter Policies](https://docs.aws.amazon.com/systems-manager/latest/userguide/parameter-store-policies.html) 