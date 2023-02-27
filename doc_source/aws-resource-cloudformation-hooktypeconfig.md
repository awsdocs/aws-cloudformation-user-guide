# AWS::CloudFormation::HookTypeConfig<a name="aws-resource-cloudformation-hooktypeconfig"></a>

The `HookTypeConfig` resource specifies the configuration of a hook\.

## Syntax<a name="aws-resource-cloudformation-hooktypeconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-hooktypeconfig-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::HookTypeConfig",
  "Properties" : {
      "[Configuration](#cfn-cloudformation-hooktypeconfig-configuration)" : String,
      "[ConfigurationAlias](#cfn-cloudformation-hooktypeconfig-configurationalias)" : String,
      "[TypeArn](#cfn-cloudformation-hooktypeconfig-typearn)" : String,
      "[TypeName](#cfn-cloudformation-hooktypeconfig-typename)" : String
    }
}
```

### YAML<a name="aws-resource-cloudformation-hooktypeconfig-syntax.yaml"></a>

```
Type: AWS::CloudFormation::HookTypeConfig
Properties: 
  [Configuration](#cfn-cloudformation-hooktypeconfig-configuration): String
  [ConfigurationAlias](#cfn-cloudformation-hooktypeconfig-configurationalias): String
  [TypeArn](#cfn-cloudformation-hooktypeconfig-typearn): String
  [TypeName](#cfn-cloudformation-hooktypeconfig-typename): String
```

## Properties<a name="aws-resource-cloudformation-hooktypeconfig-properties"></a>

`Configuration`  <a name="cfn-cloudformation-hooktypeconfig-configuration"></a>
Specifies the activated hook type configuration, in this AWS account and AWS Region\.  
You must specify either `TypeName` and `Configuration` or `TypeARN` and `Configuration`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfigurationAlias`  <a name="cfn-cloudformation-hooktypeconfig-configurationalias"></a>
Specifies the activated hook type configuration, in this AWS account and AWS Region\.  
Defaults to `default` alias\. Hook types currently support default configuration alias\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TypeArn`  <a name="cfn-cloudformation-hooktypeconfig-typearn"></a>
The Amazon Resource Number \(ARN\) for the hook to set `Configuration` for\.  
You must specify either `TypeName` and `Configuration` or `TypeARN` and `Configuration`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TypeName`  <a name="cfn-cloudformation-hooktypeconfig-typename"></a>
The unique name for your hook\. Specifies a three\-part namespace for your hook, with a recommended pattern of `Organization::Service::Hook`\.  
You must specify either `TypeName` and `Configuration` or `TypeARN` and `Configuration`\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `196`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudformation-hooktypeconfig-return-values"></a>

### Ref<a name="aws-resource-cloudformation-hooktypeconfig-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the resource version\. For example:

`arn:aws:cloudformation:us-west-2:123456789012:type-configuration/hook/My-Sample-Hook/default`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudformation-hooktypeconfig-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudformation-hooktypeconfig-return-values-fn--getatt-fn--getatt"></a>

`ConfigurationArn`  <a name="ConfigurationArn-fn::getatt"></a>
The Amazon Resource Number \(ARN\) of the activated hook type configuration, in this account and Region\.

## Examples<a name="aws-resource-cloudformation-hooktypeconfig--examples"></a>



### Specifying the configuration of a hook using TypeName<a name="aws-resource-cloudformation-hooktypeconfig--examples--Specifying_the_configuration_of_a_hook_using_TypeName"></a>

The following example demonstrates how to specify a new hook configuration with the `TypeName` property type\.

#### JSON<a name="aws-resource-cloudformation-hooktypeconfig--examples--Specifying_the_configuration_of_a_hook_using_TypeName--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "HookTypeConfig": {
            "Type": "AWS::CloudFormation::HookTypeConfig",
            "Properties": {
                "TypeName": "My::Sample::Hook",
                "Configuration": "{\"CloudFormationConfiguration\":{\"HookConfiguration\":{\"TargetStacks\":\"ALL\",\"FailureMode\":\"WARN\",\"Properties\":{\"limitSize\": \"1\",\"encryptionAlgorithm\": \"aws:kms\"}}}}"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudformation-hooktypeconfig--examples--Specifying_the_configuration_of_a_hook_using_TypeName--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  HookTypeConfig:
    Type: AWS::CloudFormation::HookTypeConfig
    Properties:
      TypeName: My::Sample::Hook
      Configuration: '{"CloudFormationConfiguration":{"HookConfiguration":{"TargetStacks":"ALL","FailureMode":"WARN","Properties":{"limitSize": "1","encryptionAlgorithm": "aws:kms"}}}}'
```

### Specifying the configuration of a hook using TypeArn<a name="aws-resource-cloudformation-hooktypeconfig--examples--Specifying_the_configuration_of_a_hook_using_TypeArn"></a>

The following example demonstrates how to specify a new hook configuration with the `TypeArn` property type\.

#### JSON<a name="aws-resource-cloudformation-hooktypeconfig--examples--Specifying_the_configuration_of_a_hook_using_TypeArn--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "HookTypeConfig": {
            "Type": "AWS::CloudFormation::HookTypeConfig",
            "Properties": {
                "TypeArn": "arn:aws:cloudformation:us-west-2:123456789012:type/hook/My-Sample-Hook",
                "Configuration": "{\"CloudFormationConfiguration\":{\"HookConfiguration\":{\"TargetStacks\":\"ALL\",\"FailureMode\":\"WARN\",\"Properties\":{\"limitSize\": \"1\",\"encryptionAlgorithm\": \"aws:kms\"}}}}"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudformation-hooktypeconfig--examples--Specifying_the_configuration_of_a_hook_using_TypeArn--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  HookTypeConfig:
    Type: AWS::CloudFormation::HookTypeConfig
    Properties:
      TypeArn: arn:aws:cloudformation:us-west-2:123456789012:type/hook/My-Sample-Hook
      Configuration: '{"CloudFormationConfiguration":{"HookConfiguration":{"TargetStacks":"ALL","FailureMode":"WARN","Properties":{"limitSize": "1","encryptionAlgorithm": "aws:kms"}}}}'
```