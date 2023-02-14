# AWS::CloudFormation::HookVersion<a name="aws-resource-cloudformation-hookversion"></a>

The `HookVersion` resource publishes new or first hook version to the AWS CloudFormation registry\.

## Syntax<a name="aws-resource-cloudformation-hookversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-hookversion-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::HookVersion",
  "Properties" : {
      "[ExecutionRoleArn](#cfn-cloudformation-hookversion-executionrolearn)" : String,
      "[LoggingConfig](#cfn-cloudformation-hookversion-loggingconfig)" : LoggingConfig,
      "[SchemaHandlerPackage](#cfn-cloudformation-hookversion-schemahandlerpackage)" : String,
      "[TypeName](#cfn-cloudformation-hookversion-typename)" : String
    }
}
```

### YAML<a name="aws-resource-cloudformation-hookversion-syntax.yaml"></a>

```
Type: AWS::CloudFormation::HookVersion
Properties: 
  [ExecutionRoleArn](#cfn-cloudformation-hookversion-executionrolearn): String
  [LoggingConfig](#cfn-cloudformation-hookversion-loggingconfig): 
    LoggingConfig
  [SchemaHandlerPackage](#cfn-cloudformation-hookversion-schemahandlerpackage): String
  [TypeName](#cfn-cloudformation-hookversion-typename): String
```

## Properties<a name="aws-resource-cloudformation-hookversion-properties"></a>

`ExecutionRoleArn`  <a name="cfn-cloudformation-hookversion-executionrolearn"></a>
The Amazon Resource Name \(ARN\) of the task execution role that grants the hook permission\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoggingConfig`  <a name="cfn-cloudformation-hookversion-loggingconfig"></a>
Contains logging configuration information for an extension\.  
*Required*: No  
*Type*: [LoggingConfig](aws-properties-cloudformation-hookversion-loggingconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SchemaHandlerPackage`  <a name="cfn-cloudformation-hookversion-schemahandlerpackage"></a>
A URL to the Amazon S3 bucket containing the hook project package that contains the necessary files for the hook you want to register\.  
For information on generating a schema handler package for the resource you want to register, see [submit](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-cli-submit.html) in the *CloudFormation CLI User Guide for Extension Development*\.  
The user registering the resource must be able to access the package in the S3 bucket\. That's, the user must have [GetObject](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html) permissions for the schema handler package\. For more information, see [Actions, Resources, and Condition Keys for Amazon S3](https://docs.aws.amazon.com/IAM/latest/UserGuide/list_amazons3.html) in the *AWS Identity and Access Management User Guide*\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TypeName`  <a name="cfn-cloudformation-hookversion-typename"></a>
The unique name for your hook\. Specifies a three\-part namespace for your hook, with a recommended pattern of `Organization::Service::Hook`\.  
The following organization namespaces are reserved and can't be used in your hook type names:  
+  `Alexa` 
+  `AMZN` 
+  `Amazon` 
+  `ASK` 
+  `AWS` 
+  `Custom` 
+  `Dev` 
*Required*: Yes  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `196`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cloudformation-hookversion-return-values"></a>

### Ref<a name="aws-resource-cloudformation-hookversion-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the resource version\. For example:

`arn:aws:cloudformation:us-west-2:012345678901:type/hook/Sample-CloudFormation-Hook/00000001`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudformation-hookversion-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudformation-hookversion-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the hook\.

`IsDefaultVersion`  <a name="IsDefaultVersion-fn::getatt"></a>
Whether the specified hook version is set as the default version\.

`TypeArn`  <a name="TypeArn-fn::getatt"></a>
The Amazon Resource Number \(ARN\) assigned to this version of the hook\.

`VersionId`  <a name="VersionId-fn::getatt"></a>
The ID of this version of the hook\.

`Visibility`  <a name="Visibility-fn::getatt"></a>
The scope at which the resource is visible and usable in CloudFormation operations\.  
Valid values include:  
+ `PRIVATE`: The resource is only visible and usable within the account in which it's registered\. CloudFormation marks any resources you register as `PRIVATE`\.
+ `PUBLIC`: The resource is publicly visible and usable within any Amazon account\.

## Examples<a name="aws-resource-cloudformation-hookversion--examples"></a>



### Specifying a hook version<a name="aws-resource-cloudformation-hookversion--examples--Specifying_a_hook_version"></a>

The following example demonstrates how to specify a new hook version\.

#### JSON<a name="aws-resource-cloudformation-hookversion--examples--Specifying_a_hook_version--json"></a>

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
        }
    }
}
```

#### YAML<a name="aws-resource-cloudformation-hookversion--examples--Specifying_a_hook_version--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  HookVersion:
    Type: 'AWS::CloudFormation::HookVersion'
    Properties:
      TypeName: 'My::Sample::Hook'
      SchemaHandlerPackage: 's3://my-sample-hookversion-bucket/my-sample-hook.zip'
```

### Specifying the default hook version<a name="aws-resource-cloudformation-hookversion--examples--Specifying_the_default_hook_version"></a>

The following example demonstrates how to specify a new hook version and use the Ref return value to set that version as the default version\.

#### JSON<a name="aws-resource-cloudformation-hookversion--examples--Specifying_the_default_hook_version--json"></a>

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

#### YAML<a name="aws-resource-cloudformation-hookversion--examples--Specifying_the_default_hook_version--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  HookVersion:
    Type: AWS::CloudFormation::HookVersion
    Properties:
      TypeName: My::Sample::Hook
      SchemaHandlerPackage: s3://my-sample-hookversion-bucket/my-sample-hook.zip
  HookDefaultVersion:
    Type: AWS::CloudFormation::HookDefaultVersion
    Properties:
      TypeVersionArn: !Ref HookVersion
```