# AWS::Batch::ComputeEnvironment LaunchTemplateSpecification<a name="aws-properties-batch-computeenvironment-launchtemplatespecification"></a>

An object representing a launch template associated with a compute resource\. You must specify either the launch template ID or launch template name in the request, but not both\.

If security groups are specified using both the `securityGroupIds` parameter of `CreateComputeEnvironment` and the launch template, the values in the `securityGroupIds` parameter of `CreateComputeEnvironment` will be used\.

**Note**  
This object isn't applicable to jobs running on Fargate resources\.

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
The version number of the launch template, `$Latest`, or `$Default`\.  
If the value is `$Latest`, the latest version of the launch template is used\. If the value is `$Default`, the default version of the launch template is used\.  
Default: `$Default`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-batch-computeenvironment-launchtemplatespecification--seealso"></a>
+  [Launch Template Support](https://docs.aws.amazon.com/batch/latest/userguide/launch-templates.html) in the *AWS Batch User Guide*\.