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