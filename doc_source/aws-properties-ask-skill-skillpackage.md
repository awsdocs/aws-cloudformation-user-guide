# Alexa::ASK::Skill SkillPackage<a name="aws-properties-ask-skill-skillpackage"></a>

The `SkillPackage` property type contains configuration details for the skill package that contains the components of the Alexa skill\. Skill packages are retrieved from an Amazon S3 bucket and key and used to create and update the skill\. More details about the skill package format are located in the [Skill Package API Reference](https://developer.amazon.com/docs/smapi/skill-package-api-reference.html#skill-package-format)\.

 `SkillPackage` is a property of the `Alexa::ASK::Skill` resource\.

## Syntax<a name="aws-properties-ask-skill-skillpackage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ask-skill-skillpackage-syntax.json"></a>

```
{
  "[Overrides](#cfn-ask-skill-skillpackage-overrides)" : Overrides,
  "[S3Bucket](#cfn-ask-skill-skillpackage-s3bucket)" : String,
  "[S3BucketRole](#cfn-ask-skill-skillpackage-s3bucketrole)" : String,
  "[S3Key](#cfn-ask-skill-skillpackage-s3key)" : String,
  "[S3ObjectVersion](#cfn-ask-skill-skillpackage-s3objectversion)" : String
}
```

### YAML<a name="aws-properties-ask-skill-skillpackage-syntax.yaml"></a>

```
  [Overrides](#cfn-ask-skill-skillpackage-overrides): 
    Overrides
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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Bucket`  <a name="cfn-ask-skill-skillpackage-s3bucket"></a>
The name of the Amazon S3 bucket where the \.zip file that contains the skill package is stored\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BucketRole`  <a name="cfn-ask-skill-skillpackage-s3bucketrole"></a>
ARN of the IAM role that grants the Alexa service \(`alexa-appkit.amazon.com`\) permission to access the bucket and retrieve the skill package\. This property is optional\. If you do not provide it, the bucket must be publicly accessible or configured with a policy that allows this access\. Otherwise, AWS CloudFormation cannot create the skill\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Key`  <a name="cfn-ask-skill-skillpackage-s3key"></a>
The location and name of the skill package \.zip file\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3ObjectVersion`  <a name="cfn-ask-skill-skillpackage-s3objectversion"></a>
If you have S3 versioning enabled, the version ID of the skill package\.zip file\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)