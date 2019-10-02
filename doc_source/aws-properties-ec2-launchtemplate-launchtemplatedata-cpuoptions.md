# AWS::EC2::LaunchTemplate CpuOptions<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-cpuoptions"></a>

Specifies the CPU options for an instance\.

 `CpuOptions` is a property of the [Amazon EC2 LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-cpuoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-cpuoptions-syntax.json"></a>

```
{
  "[CoreCount](#cfn-ec2-launchtemplate-launchtemplatedata-cpuoptions-corecount)" : Integer,
  "[ThreadsPerCore](#cfn-ec2-launchtemplate-launchtemplatedata-cpuoptions-threadspercore)" : Integer
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-cpuoptions-syntax.yaml"></a>

```
  [CoreCount](#cfn-ec2-launchtemplate-launchtemplatedata-cpuoptions-corecount): Integer
  [ThreadsPerCore](#cfn-ec2-launchtemplate-launchtemplatedata-cpuoptions-threadspercore): Integer
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-cpuoptions-properties"></a>

`CoreCount`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-cpuoptions-corecount"></a>
The number of CPU cores for the instance\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThreadsPerCore`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-cpuoptions-threadspercore"></a>
The number of CPU cores for the instance\.  
*Required*: No  
*Type*: Integer  
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
