# Alexa::ASK::Skill SkillPackage<a name="aws-properties-ask-skill-skillpackage"></a>

<a name="aws-properties-ask-skill-skillpackage-description"></a>The `SkillPackage` property type contains configuration details for the skill package that contains the components of the Alexa Skill\. Skill packages are retrieved from an Amazon S3 bucket and key and used to create and update the skill\. More details about the skill package format are located in the [Skill Package API Reference](https://developer.amazon.com/docs/smapi/skill-package-api-reference.html#skill-package-format)\.

<a name="aws-properties-ask-skill-skillpackage-inheritance"></a> `SkillPackage` is a property of the [Alexa::ASK::Skill](aws-resource-ask-skill.md) resource\.

## Syntax<a name="aws-properties-ask-skill-skillpackage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ask-skill-skillpackage-syntax.json"></a>

```
{
  "[Overrides](#cfn-ask-skill-skillpackage-overrides)" : [*Overrides*](aws-properties-ask-skill-overrides.md),
  "[S3Bucket](#cfn-ask-skill-skillpackage-s3bucket)" : String,
  "[S3BucketRole](#cfn-ask-skill-skillpackage-s3bucketrole)" : String,
  "[S3Key](#cfn-ask-skill-skillpackage-s3key)" : String,
  "[S3ObjectVersion](#cfn-ask-skill-skillpackage-s3objectversion)" : String
}
```

### YAML<a name="aws-properties-ask-skill-skillpackage-syntax.yaml"></a>

```
[Overrides](#cfn-ask-skill-skillpackage-overrides): 
  [*Overrides*](aws-properties-ask-skill-overrides.md)
[S3Bucket](#cfn-ask-skill-skillpackage-s3bucket): String
[S3BucketRole](#cfn-ask-skill-skillpackage-s3bucketrole): String
[S3Key](#cfn-ask-skill-skillpackage-s3key): String
[S3ObjectVersion](#cfn-ask-skill-skillpackage-s3objectversion): String
```

## Properties<a name="aws-properties-ask-skill-skillpackage-properties"></a>

`Overrides`  <a name="cfn-ask-skill-skillpackage-overrides"></a>
Overrides to the skill package to apply when creating or updating the skill\. Values provided here do not modify the contents of the original skill package\. Currently, only overriding values inside of the skill manifest component of the package is supported\.  
 *Required*: No  
 *Type*: [Overrides](aws-properties-ask-skill-overrides.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3Bucket`  <a name="cfn-ask-skill-skillpackage-s3bucket"></a>
The name of the Amazon S3 bucket where the \.zip file that contains the skill package is stored\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3BucketRole`  <a name="cfn-ask-skill-skillpackage-s3bucketrole"></a>
ARN of the role that grants the Alexa service permission to access the bucket and retrieve the skill package\. This role is optional, and if not provided the bucket must be configured with a policy allowing this access, or be publicly accessible, in order for AWS CloudFormation to create the skill\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3Key`  <a name="cfn-ask-skill-skillpackage-s3key"></a>
The location and name of the skill package \.zip file\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3ObjectVersion`  <a name="cfn-ask-skill-skillpackage-s3objectversion"></a>
If you have S3 versioning enabled, the version ID of the skill package\.zip file\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 