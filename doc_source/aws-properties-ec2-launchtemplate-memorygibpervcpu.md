# AWS::EC2::LaunchTemplate MemoryGiBPerVCpu<a name="aws-properties-ec2-launchtemplate-memorygibpervcpu"></a>

The minimum and maximum amount of memory per vCPU, in GiB\.

## Syntax<a name="aws-properties-ec2-launchtemplate-memorygibpervcpu-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-memorygibpervcpu-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-launchtemplate-memorygibpervcpu-max)" : Double,
  "[Min](#cfn-ec2-launchtemplate-memorygibpervcpu-min)" : Double
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-memorygibpervcpu-syntax.yaml"></a>

```
  [Max](#cfn-ec2-launchtemplate-memorygibpervcpu-max): Double
  [Min](#cfn-ec2-launchtemplate-memorygibpervcpu-min): Double
```

## Properties<a name="aws-properties-ec2-launchtemplate-memorygibpervcpu-properties"></a>

`Max`  <a name="cfn-ec2-launchtemplate-memorygibpervcpu-max"></a>
The maximum amount of memory per vCPU, in GiB\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-ec2-launchtemplate-memorygibpervcpu-min"></a>
The minimum amount of memory per vCPU, in GiB\. To specify no minimum limit, omit this parameter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)