# AWS::Batch::ComputeEnvironment LaunchTemplateSpecification<a name="aws-properties-batch-computeenvironment-launchtemplatespecification"></a>

An object representing a launch template associated with a compute resource\. You must specify either the launch template ID or launch template name in the request, but not both\. 

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
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchTemplateName`  <a name="cfn-batch-computeenvironment-launchtemplatespecification-launchtemplatename"></a>
The name of the launch template\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Version`  <a name="cfn-batch-computeenvironment-launchtemplatespecification-version"></a>
The version number of the launch template\.  
Default: The default version of the launch template\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See Also<a name="aws-properties-batch-computeenvironment-launchtemplatespecification--seealso"></a>
+  [Launch Template Support](https://docs.aws.amazon.com/batch/latest/userguide/launch-templates.html) in the *AWS Batch User Guide*\.

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
