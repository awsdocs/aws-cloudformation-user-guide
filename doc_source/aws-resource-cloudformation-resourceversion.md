# AWS::CloudFormation::ResourceVersion<a name="aws-resource-cloudformation-resourceversion"></a>

Registers a resource version with the CloudFormation service\. Registering a resource version makes it available for use in CloudFormation templates in your AWS account, and includes:
+ Validating the resource schema\.
+ Determining which handlers, if any, have been specified for the resource\.
+ Making the resource available for use in your account\.

For more information on how to develop resources and ready them for registration, see [Creating Resource Providers](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-types.html) in the *CloudFormation CLI User Guide*\.

You can have a maximum of 50 resource versions registered at a time\. This maximum is per account and per Region\.

## Syntax<a name="aws-resource-cloudformation-resourceversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-resourceversion-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::ResourceVersion",
  "Properties" : {
      "[ExecutionRoleArn](#cfn-cloudformation-resourceversion-executionrolearn)" : String,
      "[LoggingConfig](#cfn-cloudformation-resourceversion-loggingconfig)" : LoggingConfig,
      "[SchemaHandlerPackage](#cfn-cloudformation-resourceversion-schemahandlerpackage)" : String,
      "[TypeName](#cfn-cloudformation-resourceversion-typename)" : String
    }
}
```

### YAML<a name="aws-resource-cloudformation-resourceversion-syntax.yaml"></a>

```
Type: AWS::CloudFormation::ResourceVersion
Properties: 
  [ExecutionRoleArn](#cfn-cloudformation-resourceversion-executionrolearn): String
  [LoggingConfig](#cfn-cloudformation-resourceversion-loggingconfig): 
    LoggingConfig
  [SchemaHandlerPackage](#cfn-cloudformation-resourceversion-schemahandlerpackage): String
  [TypeName](#cfn-cloudformation-resourceversion-typename): String
```

## Properties<a name="aws-resource-cloudformation-resourceversion-properties"></a>

`ExecutionRoleArn`  <a name="cfn-cloudformation-resourceversion-executionrolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role for CloudFormation to assume when invoking the resource\. If your resource calls AWS APIs in any of its handlers, you must create an *[IAM execution role](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html)* that includes the necessary permissions to call those AWS APIs, and provision that execution role in your account\. When CloudFormation needs to invoke the resource type handler, CloudFormation assumes this execution role to create a temporary session token, which it then passes to the resource type handler, thereby supplying your resource type with the appropriate credentials\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `arn:.+:iam::[0-9]{12}:role/.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoggingConfig`  <a name="cfn-cloudformation-resourceversion-loggingconfig"></a>
Logging configuration information for a resource\.  
*Required*: No  
*Type*: [LoggingConfig](aws-properties-cloudformation-resourceversion-loggingconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SchemaHandlerPackage`  <a name="cfn-cloudformation-resourceversion-schemahandlerpackage"></a>
A URL to the S3 bucket containing the resource project package that contains the necessary files for the resource you want to register\.  
For information on generating a schema handler package for the resource you want to register, see [submit](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-cli-submit.html) in the *CloudFormation CLI User Guide*\.  
The user registering the resource must be able to access the package in the S3 bucket\. That is, the user needs to have [GetObject](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html) permissions for the schema handler package\. For more information, see [Actions, Resources, and Condition Keys for Amazon S3](https://docs.aws.amazon.com/IAM/latest/UserGuide/list_amazons3.html) in the *AWS Identity and Access Management User Guide*\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TypeName`  <a name="cfn-cloudformation-resourceversion-typename"></a>
The name of the resource being registered\.  
We recommend that resource names adhere to the following pattern: *company\_or\_organization*::*service*::*type*\.  
The following organization namespaces are reserved and can't be used in your resource names:  
+ `Alexa`
+ `AMZN`
+ `Amazon`
+ `AWS`
+ `Custom`
+ `Dev`
*Required*: Yes  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `204`  
*Pattern*: `[A-Za-z0-9]{2,64}::[A-Za-z0-9]{2,64}::[A-Za-z0-9]{2,64}(::MODULE){0,1}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cloudformation-resourceversion-return-values"></a>

### Ref<a name="aws-resource-cloudformation-resourceversion-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the resource version\. For example:

`arn:aws:cloudformation:us-west-2:012345678901:type/resource/Sample-CloudFormation-Resource/00000001`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudformation-resourceversion-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudformation-resourceversion-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the resource version\.

`IsDefaultVersion`  <a name="IsDefaultVersion-fn::getatt"></a>
Whether the resource version is set as the default version\.

`ProvisioningType`  <a name="ProvisioningType-fn::getatt"></a>
The provisioning behavior of the resource type\. CloudFormation determines the provisioning type during registration, based on the types of handlers in the schema handler package submitted\.  
Valid values include:  
+ `FULLY_MUTABLE`: The resource type includes an update handler to process updates to the type during stack update operations\.
+ `IMMUTABLE`: The resource type doesn't include an update handler, so the type can't be updated and must instead be replaced during stack update operations\.
+ `NON_PROVISIONABLE`: The resource type doesn't include all the following handlers, and therefore can't actually be provisioned\.
  + create
  + read
  + delete

`TypeArn`  <a name="TypeArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the resource\.

`VersionId`  <a name="VersionId-fn::getatt"></a>
The ID of a specific version of the resource\. The version ID is the value at the end of the Amazon Resource Name \(ARN\) assigned to the resource version when it is registered\.

`Visibility`  <a name="Visibility-fn::getatt"></a>
The scope at which the resource is visible and usable in CloudFormation operations\.  
Valid values include:  
+ `PRIVATE`: The resource is only visible and usable within the account in which it's registered\. CloudFormation marks any resources you register as `PRIVATE`\.
+ `PUBLIC`: The resource is publicly visible and usable within any Amazon account\.

## Examples<a name="aws-resource-cloudformation-resourceversion--examples"></a>



### Specifying a resource version<a name="aws-resource-cloudformation-resourceversion--examples--Specifying_a_resource_version"></a>

The following example demonstrates how to specify a new resource version\.

#### JSON<a name="aws-resource-cloudformation-resourceversion--examples--Specifying_a_resource_version--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "ResourceVersion": {
            "Type": "AWS::CloudFormation::ResourceVersion",
            "Properties": {
                "TypeName": "My::Sample::Resource",
                "SchemaHandlerPackage": "s3://my-sample-resourceversion-bucket/my-sample-resource.zip"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudformation-resourceversion--examples--Specifying_a_resource_version--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  ResourceVersion:
    Type: AWS::CloudFormation::ResourceVersion
    Properties:
      TypeName: My::Sample::Resource
      SchemaHandlerPackage: s3://my-sample-resourceversion-bucket/my-sample-resource.zip
```

### Specifying a resource version and setting it as the default version<a name="aws-resource-cloudformation-resourceversion--examples--Specifying_a_resource_version_and_setting_it_as_the_default_version"></a>

The following example demonstrates how to specify and new resource version, and use the `Ref` return value to set that version as the default version\.

#### JSON<a name="aws-resource-cloudformation-resourceversion--examples--Specifying_a_resource_version_and_setting_it_as_the_default_version--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "ResourceVersion": {
            "Type": "AWS::CloudFormation::ResourceVersion",
            "Properties": {
                "TypeName": "My::Sample::Resource",
                "SchemaHandlerPackage": "s3://my-sample-resourceversion-bucket/my-sample-resource.zip"
            }
        },
        "ResourceDefaultVersion": {
            "Type": "AWS::CloudFormation::ResourceDefaultVersion",
            "Properties": {
                "TypeVersionArn": {
                    "Ref": "ResourceVersion"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudformation-resourceversion--examples--Specifying_a_resource_version_and_setting_it_as_the_default_version--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  ResourceVersion:
    Type: AWS::CloudFormation::ResourceVersion
    Properties:
      TypeName: My::Sample::Resource
      SchemaHandlerPackage: s3://my-sample-resourceversion-bucket/my-sample-resource.zip
  ResourceDefaultVersion:
    Type: AWS::CloudFormation::ResourceDefaultVersion
    Properties:
      TypeVersionArn: !Ref ResourceVersion
```