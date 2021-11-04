# AWS::EC2::LaunchTemplate AcceleratorCount<a name="aws-properties-ec2-launchtemplate-acceleratorcount"></a>

The minimum and maximum number of accelerators \(GPUs, FPGAs, or AWS Inferentia chips\) on an instance\.

## Syntax<a name="aws-properties-ec2-launchtemplate-acceleratorcount-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-acceleratorcount-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-launchtemplate-acceleratorcount-max)" : Integer,
  "[Min](#cfn-ec2-launchtemplate-acceleratorcount-min)" : Integer
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-acceleratorcount-syntax.yaml"></a>

```
  [Max](#cfn-ec2-launchtemplate-acceleratorcount-max): Integer
  [Min](#cfn-ec2-launchtemplate-acceleratorcount-min): Integer
```

## Properties<a name="aws-properties-ec2-launchtemplate-acceleratorcount-properties"></a>

`Max`  <a name="cfn-ec2-launchtemplate-acceleratorcount-max"></a>
The maximum number of accelerators\. To specify no maximum limit, omit this parameter\. To exclude accelerator\-enabled instance types, set `Max` to `0`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-ec2-launchtemplate-acceleratorcount-min"></a>
The minimum number of accelerators\. To specify no minimum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)