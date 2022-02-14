# AWS::CloudFormation::HookDefaultVersion<a name="aws-resource-cloudformation-hookdefaultversion"></a>

The `HookDefaultVersion` resource specifies the default version of the hook\. The default version of the hook is used in CloudFormation operations for this AWS account and AWS Region\.

## Syntax<a name="aws-resource-cloudformation-hookdefaultversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-hookdefaultversion-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::HookDefaultVersion",
  "Properties" : {
      "[TypeName](#cfn-cloudformation-hookdefaultversion-typename)" : String,
      "[TypeVersionArn](#cfn-cloudformation-hookdefaultversion-typeversionarn)" : String,
      "[VersionId](#cfn-cloudformation-hookdefaultversion-versionid)" : String
    }
}
```

### YAML<a name="aws-resource-cloudformation-hookdefaultversion-syntax.yaml"></a>

```
Type: AWS::CloudFormation::HookDefaultVersion
Properties: 
  [TypeName](#cfn-cloudformation-hookdefaultversion-typename): String
  [TypeVersionArn](#cfn-cloudformation-hookdefaultversion-typeversionarn): String
  [VersionId](#cfn-cloudformation-hookdefaultversion-versionid): String
```

## Properties<a name="aws-resource-cloudformation-hookdefaultversion-properties"></a>

`TypeName`  <a name="cfn-cloudformation-hookdefaultversion-typename"></a>
The name of the hook\.  
You must specify either `TypeVersionArn`, or `TypeName` and `VersionId`\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TypeVersionArn`  <a name="cfn-cloudformation-hookdefaultversion-typeversionarn"></a>
The version ID of the type configuration\.  
You must specify either `TypeVersionArn`, or `TypeName` and `VersionId`\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[A-Za-z0-9-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VersionId`  <a name="cfn-cloudformation-hookdefaultversion-versionid"></a>
The version ID of the type specified\.  
You must specify either `TypeVersionArn`, or `TypeName` and `VersionId`\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[A-Za-z0-9-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudformation-hookdefaultversion-return-values"></a>

### Ref<a name="aws-resource-cloudformation-hookdefaultversion-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the resource version\. For example:

`arn:aws:cloudformation:us-west-2:012345678901:type/hook/Sample-CloudFormation-Hook/00000001`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudformation-hookdefaultversion-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudformation-hookdefaultversion-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Number \(ARN\) of the activated extension, in this account and Region\.

## Examples<a name="aws-resource-cloudformation-hookdefaultversion--examples"></a>



### Specifying a hook default version<a name="aws-resource-cloudformation-hookdefaultversion--examples--Specifying_a_hook_default_version"></a>

The following example demonstrates how to specify a new hook version and use the Ref return value to set that version as the default version\.

#### JSON<a name="aws-resource-cloudformation-hookdefaultversion--examples--Specifying_a_hook_default_version--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "HookVersion": {
            "Type": "AWS::CloudFormation::HookVersion",
            "Properties": {
                "TypeName": "My::Sample::Hook",
                "SchemaHandlerPackage": "s3://my-sample-hookversion-bucket/my-sample-hook.zip"
            }
        },
        "HookDefaultVersion": {
            "Type": "AWS::CloudFormation::HookDefaultVersion",
            "Properties": {
                "TypeVersionArn": {
                    "Ref": "HookVersion"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudformation-hookdefaultversion--examples--Specifying_a_hook_default_version--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  HookVersion:
    Type: 'AWS::CloudFormation::HookVersion'
    Properties:
      TypeName: 'My::Sample::Hook'
      SchemaHandlerPackage: 's3://my-sample-hookversion-bucket/my-sample-hook.zip'
  HookDefaultVersion:
    Type: 'AWS::CloudFormation::HookDefaultVersion'
    Properties:
      TypeVersionArn: !Ref HookVersion
```

### Specifying a hook default version using TypeVersionArn<a name="aws-resource-cloudformation-hookdefaultversion--examples--Specifying_a_hook_default_version_using_TypeVersionArn"></a>

The following example demonstrates how to set a hook version as the default version through the `TypeVersionArn` property type\.

#### JSON<a name="aws-resource-cloudformation-hookdefaultversion--examples--Specifying_a_hook_default_version_using_TypeVersionArn--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "HookDefaultVersion": {
            "Type": "AWS::CloudFormation::HookDefaultVersion",
            "Properties": {
                "TypeVersionArn": "arn:aws:cloudformation:us-west-2:123456789012:type/hook/My-Sample-Hook/00000001"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudformation-hookdefaultversion--examples--Specifying_a_hook_default_version_using_TypeVersionArn--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  HookDefaultVersion:
    Type: 'AWS::CloudFormation::HookDefaultVersion'
    Properties:
      TypeVersionArn: >-
        arn:aws:cloudformation:us-west-2:123456789012:type/hook/My-Sample-Hook/00000001
```

### Specifying a hook default version using TypeName and VersionId<a name="aws-resource-cloudformation-hookdefaultversion--examples--Specifying_a_hook_default_version_using_TypeName_and_VersionId"></a>

The following example demonstrates how to set a hook version as the default version through the `VersionId` property type\.

#### JSON<a name="aws-resource-cloudformation-hookdefaultversion--examples--Specifying_a_hook_default_version_using_TypeName_and_VersionId--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "HookDefaultVersion": {
            "Type": "AWS::CloudFormation::HookDefaultVersion",
            "Properties": {
                "TypeName": "My::Sample::Hook",
                "VersionId": 1
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudformation-hookdefaultversion--examples--Specifying_a_hook_default_version_using_TypeName_and_VersionId--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  HookDefaultVersion:
    Type: 'AWS::CloudFormation::HookDefaultVersion'
    Properties:
      TypeName: 'My::Sample::Hook'
      VersionId: 1
```