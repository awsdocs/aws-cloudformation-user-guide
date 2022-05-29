# AWS::CloudFormation::ResourceDefaultVersion<a name="aws-resource-cloudformation-resourcedefaultversion"></a>

Specifies the default version of a resource\. The default version of a resource will be used in CloudFormation operations\.

## Syntax<a name="aws-resource-cloudformation-resourcedefaultversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-resourcedefaultversion-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::ResourceDefaultVersion",
  "Properties" : {
      "[TypeName](#cfn-cloudformation-resourcedefaultversion-typename)" : String,
      "[TypeVersionArn](#cfn-cloudformation-resourcedefaultversion-typeversionarn)" : String,
      "[VersionId](#cfn-cloudformation-resourcedefaultversion-versionid)" : String
    }
}
```

### YAML<a name="aws-resource-cloudformation-resourcedefaultversion-syntax.yaml"></a>

```
Type: AWS::CloudFormation::ResourceDefaultVersion
Properties: 
  [TypeName](#cfn-cloudformation-resourcedefaultversion-typename): String
  [TypeVersionArn](#cfn-cloudformation-resourcedefaultversion-typeversionarn): String
  [VersionId](#cfn-cloudformation-resourcedefaultversion-versionid): String
```

## Properties<a name="aws-resource-cloudformation-resourcedefaultversion-properties"></a>

`TypeName`  <a name="cfn-cloudformation-resourcedefaultversion-typename"></a>
The name of the resource\.  
Conditional: You must specify either `TypeVersionArn`, or `TypeName` and `VersionId`\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `204`  
*Pattern*: `[A-Za-z0-9]{2,64}::[A-Za-z0-9]{2,64}::[A-Za-z0-9]{2,64}(::MODULE){0,1}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TypeVersionArn`  <a name="cfn-cloudformation-resourcedefaultversion-typeversionarn"></a>
The Amazon Resource Name \(ARN\) of the resource version\.  
Conditional: You must specify either `TypeVersionArn`, or `TypeName` and `VersionId`\.  
*Required*: Conditional  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `arn:aws[A-Za-z0-9-]{0,64}:cloudformation:[A-Za-z0-9-]{1,64}:[0-9]{12}:type/.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VersionId`  <a name="cfn-cloudformation-resourcedefaultversion-versionid"></a>
The ID of a specific version of the resource\. The version ID is the value at the end of the Amazon Resource Name \(ARN\) assigned to the resource version when it's registered\.  
Conditional: You must specify either `TypeVersionArn`, or `TypeName` and `VersionId`\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[A-Za-z0-9-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudformation-resourcedefaultversion-return-values"></a>

### Ref<a name="aws-resource-cloudformation-resourcedefaultversion-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the resource type\. For example:

`arn:aws:cloudformation:us-west-2:012345678910:type/resource/Sample-CloudFormation-Resource`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudformation-resourcedefaultversion-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudformation-resourcedefaultversion-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the resource\.

## Examples<a name="aws-resource-cloudformation-resourcedefaultversion--examples"></a>



### Specifying a resource version and setting it as the default version<a name="aws-resource-cloudformation-resourcedefaultversion--examples--Specifying_a_resource_version_and_setting_it_as_the_default_version"></a>

The following example demonstrates how to specify and new resource version, and use the `Ref` return value to set that version as the default version\.

#### JSON<a name="aws-resource-cloudformation-resourcedefaultversion--examples--Specifying_a_resource_version_and_setting_it_as_the_default_version--json"></a>

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

#### YAML<a name="aws-resource-cloudformation-resourcedefaultversion--examples--Specifying_a_resource_version_and_setting_it_as_the_default_version--yaml"></a>

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