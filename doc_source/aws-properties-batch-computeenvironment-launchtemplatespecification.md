# AWS Batch ComputeEnvironment LaunchTemplateSpecification<a name="aws-properties-batch-computeenvironment-launchtemplatespecification"></a>

<a name="aws-properties-batch-computeenvironment-launchtemplatespecification-description"></a>The `LaunchTemplateSpecification` property type specifies a launch template to use with your compute environment\.

<a name="aws-properties-batch-computeenvironment-launchtemplatespecification-inheritance"></a> `LaunchTemplateSpecification` is a property of the [ComputeResources](aws-properties-batch-computeenvironment-computeresources.md) property type\.

## Syntax<a name="aws-properties-batch-computeenvironment-launchtemplatespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-computeenvironment-launchtemplatespecification-syntax.json"></a>

```
{
  "[LaunchTemplateId](#cfn-batch-computeenvironment-launchtemplatespecification-launchtemplateid)" : String,
  "[LaunchTemplateName](#cfn-batch-computeenvironment-launchtemplatespecification-launchtemplatename)" : String,
  "[Version](#cfn-batch-computeenvironment-launchtemplatespecification-version)" : String
}
```

### YAML<a name="aws-properties-batch-computeenvironment-launchtemplatespecification-syntax.yaml"></a>

```
[LaunchTemplateId](#cfn-batch-computeenvironment-launchtemplatespecification-launchtemplateid): String
[LaunchTemplateName](#cfn-batch-computeenvironment-launchtemplatespecification-launchtemplatename): String
[Version](#cfn-batch-computeenvironment-launchtemplatespecification-version): String
```

## Properties<a name="aws-properties-batch-computeenvironment-launchtemplatespecification-properties"></a>

`LaunchTemplateId`  <a name="cfn-batch-computeenvironment-launchtemplatespecification-launchtemplateid"></a>
The ID of the launch template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`LaunchTemplateName`  <a name="cfn-batch-computeenvironment-launchtemplatespecification-launchtemplatename"></a>
The name of the launch template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Version`  <a name="cfn-batch-computeenvironment-launchtemplatespecification-version"></a>
The version number of the launch template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-batch-computeenvironment-launchtemplatespecification-seealso"></a>
+ [Launch Template Support](https://docs.aws.amazon.com/batch/latest/userguide/launch-templates.html) in the *AWS Batch User Guide*