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
  [Type](#cfn-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator-type): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator-properties"></a>

`Type`  <a name="cfn-ec2-launchtemplate-launchtemplateelasticinferenceaccelerator-type"></a>
 The type of elastic inference accelerator\. The possible values are eia1\.medium, eia1\.large, and eia1\.xlarge\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-east-1`
- `ap-northeast-1`
- `ap-northeast-2`
- `ap-northeast-3`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `cn-north-1`
- `cn-northwest-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-gov-east-1`
- `us-gov-west-1`
- `us-west-1`
- `us-west-2`
