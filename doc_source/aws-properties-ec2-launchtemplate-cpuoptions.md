# AWS::EC2::LaunchTemplate CpuOptions<a name="aws-properties-ec2-launchtemplate-cpuoptions"></a>

Specifies the CPU options for an instance\. For more information, see [Optimize CPU options](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-optimize-cpu.html) in the *Amazon Elastic Compute Cloud User Guide*\.

 `CpuOptions` is a property of [AWS::EC2::LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-cpuoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-cpuoptions-syntax.json"></a>

```
{
  "[AmdSevSnp](#cfn-ec2-launchtemplate-cpuoptions-amdsevsnp)" : String,
  "[CoreCount](#cfn-ec2-launchtemplate-cpuoptions-corecount)" : Integer,
  "[ThreadsPerCore](#cfn-ec2-launchtemplate-cpuoptions-threadspercore)" : Integer
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-cpuoptions-syntax.yaml"></a>

```
  [AmdSevSnp](#cfn-ec2-launchtemplate-cpuoptions-amdsevsnp): String
  [CoreCount](#cfn-ec2-launchtemplate-cpuoptions-corecount): Integer
  [ThreadsPerCore](#cfn-ec2-launchtemplate-cpuoptions-threadspercore): Integer
```

## Properties<a name="aws-properties-ec2-launchtemplate-cpuoptions-properties"></a>

`AmdSevSnp`  <a name="cfn-ec2-launchtemplate-cpuoptions-amdsevsnp"></a>
Indicates whether to enable the instance for AMD SEV\-SNP\. AMD SEV\-SNP is supported with M6a, R6a, and C6a instance types only\. For more information, see [AMD SEV\-SNP](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/sev-snp.html)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `disabled | enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CoreCount`  <a name="cfn-ec2-launchtemplate-cpuoptions-corecount"></a>
The number of CPU cores for the instance\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThreadsPerCore`  <a name="cfn-ec2-launchtemplate-cpuoptions-threadspercore"></a>
The number of threads per CPU core\. To disable multithreading for the instance, specify a value of `1`\. Otherwise, specify the default value of `2`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-launchtemplate-cpuoptions--seealso"></a>
+ [Optimize CPU options](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-optimize-cpu.html) in the *Amazon EC2 User Guide*\.