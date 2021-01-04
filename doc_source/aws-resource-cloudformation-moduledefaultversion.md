# AWS::CloudFormation::ModuleDefaultVersion<a name="aws-resource-cloudformation-moduledefaultversion"></a>

Specifies the default version of a module\. The default version of the module will be used in CloudFormation operations for this account and region\.

To register a module version, use the `[AWS::CloudFormation::ModuleVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-moduleversion.html)` resource\.

For more information using modules, see [Using modules to encapsulate and reuse resource configurations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/modules.html) and [Registering extensions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html#registry-register) in the *CloudFormation User Guide*\. For information on developing modules, see [Developing modules](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/modules.html) in the *CloudFormation CLI User Guide*\. 

## Syntax<a name="aws-resource-cloudformation-moduledefaultversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-moduledefaultversion-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::ModuleDefaultVersion",
  "Properties" : {
      "[Arn](#cfn-cloudformation-moduledefaultversion-arn)" : String,
      "[ModuleName](#cfn-cloudformation-moduledefaultversion-modulename)" : String,
      "[VersionId](#cfn-cloudformation-moduledefaultversion-versionid)" : String
    }
}
```

### YAML<a name="aws-resource-cloudformation-moduledefaultversion-syntax.yaml"></a>

```
Type: AWS::CloudFormation::ModuleDefaultVersion
Properties: 
  [Arn](#cfn-cloudformation-moduledefaultversion-arn): String
  [ModuleName](#cfn-cloudformation-moduledefaultversion-modulename): String
  [VersionId](#cfn-cloudformation-moduledefaultversion-versionid): String
```

## Properties<a name="aws-resource-cloudformation-moduledefaultversion-properties"></a>

`Arn`  <a name="cfn-cloudformation-moduledefaultversion-arn"></a>
The Amazon Resource Name \(ARN\) of the module version to set as the default version\.  
Conditional: You must specify either `Arn`, or `ModuleName` and `VersionId`\.  
*Required*: Conditional  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `arn:aws[A-Za-z0-9-]{0,64}:cloudformation:[A-Za-z0-9-]{1,64}:[0-9]{12}:type/.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModuleName`  <a name="cfn-cloudformation-moduledefaultversion-modulename"></a>
The name of the module\.  
Conditional: You must specify either `Arn`, or `ModuleName` and `VersionId`\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `204`  
*Pattern*: `[A-Za-z0-9]{2,64}::[A-Za-z0-9]{2,64}::[A-Za-z0-9]{2,64}(::MODULE){0,1}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VersionId`  <a name="cfn-cloudformation-moduledefaultversion-versionid"></a>
The ID for the specific version of the module\.  
Conditional: You must specify either `Arn`, or `ModuleName` and `VersionId`\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[A-Za-z0-9-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cloudformation-moduledefaultversion-return-values"></a>

### Ref<a name="aws-resource-cloudformation-moduledefaultversion-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the module version\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Remarks<a name="aws-resource-cloudformation-moduledefaultversion--remarks"></a>

Considerations when managing the default module version:
+ The first module version to be registered in an account and region remains the default version CloudFormation uses, unless and until you explicitly sets another version as the default\.
+ For ease of determining which module version is the default version, we recommend that you only include a single `AWS::CloudFormation::ModuleDefaultVersion` resource for a given module in a template\.
+ If you delete an `AWS::CloudFormation::ModuleVersion` resource, either by deleting it from a stack or deleting the entire stack, CloudFormation marks the corresponding module version as `DEPRECATED`\.

  If you attempt to delete an `AWS::CloudFormation::ModuleVersion` resource that represent the default version, the operation will fail if there are other active versions\.

  For more information on deprecating module versions, see [DeregisterType](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DeregisterType.html) in the *AWS CloudFormation API Reference*\.

## Examples<a name="aws-resource-cloudformation-moduledefaultversion--examples"></a>

### Specifying the default module version<a name="aws-resource-cloudformation-moduledefaultversion--examples--Specifying_the_default_module_version"></a>

The following example registers two versions of a module, and then sets the second version as the default version for CloudFormation to use\. Note that the example uses the `DependsOn` attribute to ensure that CloudFormation provisions version one before version two\. 

#### YAML<a name="aws-resource-cloudformation-moduledefaultversion--examples--Specifying_the_default_module_version--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  ModuleVersion1:
    Type: 'AWS::CloudFormation::ModuleVersion'
    Properties:
      ModuleName: 'My::Sample::Test::MODULE'
      ModulePackage: 's3://my-sample-moduleversion-bucket/sample-module-package-v1.zip'
  ModuleVersion2:
    Type: 'AWS::CloudFormation::ModuleVersion'
    Properties:
      ModuleName: 'My::Sample::Test::MODULE'
      ModulePackage: 's3://my-sample-moduleversion-bucket/sample-module-package-v2.zip'
    DependsOn: ModuleVersion1
  ModuleDefaultVersion:
    Type: 'AWS::CloudFormation::ModuleDefaultVersion'
    Properties:
      Arn: !Ref ModuleVersion2
```

#### JSON<a name="aws-resource-cloudformation-moduledefaultversion--examples--Specifying_the_default_module_version--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "ModuleVersion1": {
            "Type": "AWS::CloudFormation::ModuleVersion",
            "Properties": {
                "ModuleName": "My::Sample::Test::MODULE",
                "ModulePackage": "s3://my-sample-moduleversion-bucket/sample-module-package-v1.zip"
            }
        },
        "ModuleVersion2": {
            "Type": "AWS::CloudFormation::ModuleVersion",
            "Properties": {
                "ModuleName": "My::Sample::Test::MODULE",
                "ModulePackage": "s3://my-sample-moduleversion-bucket/sample-module-package-v2.zip"
            },
            "DependsOn": "ModuleVersion1"
        },
        "ModuleDefaultVersion": {
            "Type": "AWS::CloudFormation::ModuleDefaultVersion",
            "Properties": {
                "Arn": {
                    "Ref": "ModuleVersion2"
                }
            }
        }
    }
}
```