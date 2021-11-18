# AWS::EC2::LaunchTemplate MemoryMiB<a name="aws-properties-ec2-launchtemplate-memorymib"></a>

The minimum and maximum amount of memory, in MiB\.

## Syntax<a name="aws-properties-ec2-launchtemplate-memorymib-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-memorymib-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-launchtemplate-memorymib-max)" : Integer,
  "[Min](#cfn-ec2-launchtemplate-memorymib-min)" : Integer
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-memorymib-syntax.yaml"></a>

```
  [Max](#cfn-ec2-launchtemplate-memorymib-max): Integer
  [Min](#cfn-ec2-launchtemplate-memorymib-min): Integer
```

## Properties<a name="aws-properties-ec2-launchtemplate-memorymib-properties"></a>

`Max`  <a name="cfn-ec2-launchtemplate-memorymib-max"></a>
The maximum amount of memory, in MiB\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-ec2-launchtemplate-memorymib-min"></a>
The minimum amount of memory, in MiB\. To specify no minimum limit, specify `0`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)