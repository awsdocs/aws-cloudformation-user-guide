# AWS::EC2::LaunchTemplate AcceleratorTotalMemoryMiB<a name="aws-properties-ec2-launchtemplate-acceleratortotalmemorymib"></a>

The minimum and maximum amount of total accelerator memory, in MiB\.

## Syntax<a name="aws-properties-ec2-launchtemplate-acceleratortotalmemorymib-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-acceleratortotalmemorymib-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-launchtemplate-acceleratortotalmemorymib-max)" : Integer,
  "[Min](#cfn-ec2-launchtemplate-acceleratortotalmemorymib-min)" : Integer
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-acceleratortotalmemorymib-syntax.yaml"></a>

```
  [Max](#cfn-ec2-launchtemplate-acceleratortotalmemorymib-max): Integer
  [Min](#cfn-ec2-launchtemplate-acceleratortotalmemorymib-min): Integer
```

## Properties<a name="aws-properties-ec2-launchtemplate-acceleratortotalmemorymib-properties"></a>

`Max`  <a name="cfn-ec2-launchtemplate-acceleratortotalmemorymib-max"></a>
The maximum amount of accelerator memory, in MiB\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-ec2-launchtemplate-acceleratortotalmemorymib-min"></a>
The minimum amount of accelerator memory, in MiB\. To specify no minimum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)