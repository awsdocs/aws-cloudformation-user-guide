# AWS::EC2::LaunchTemplate LaunchTemplateElasticInferenceAccelerator<a name="aws-properties-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator"></a>

Specifies an elastic inference accelerator\.

 `LaunchTemplateElasticInferenceAccelerator` is a property of the [Amazon EC2 LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator-syntax.json"></a>

```
{
  "[Type](#cfn-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator-type)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator-syntax.yaml"></a>

```
﻿  [Type](#cfn-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator-type) : String
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator-properties"></a>

`Type`  <a name="cfn-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator-type"></a>
 The type of elastic inference accelerator\. The possible values are eia1\.medium, eia1\.large, and eia1\.xlarge\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)