# AWS::EC2::EC2Fleet AcceleratorTotalMemoryMiBRequest<a name="aws-properties-ec2-ec2fleet-acceleratortotalmemorymibrequest"></a>

The minimum and maximum amount of total accelerator memory, in MiB\.

## Syntax<a name="aws-properties-ec2-ec2fleet-acceleratortotalmemorymibrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-acceleratortotalmemorymibrequest-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-ec2fleet-acceleratortotalmemorymibrequest-max)" : Integer,
  "[Min](#cfn-ec2-ec2fleet-acceleratortotalmemorymibrequest-min)" : Integer
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-acceleratortotalmemorymibrequest-syntax.yaml"></a>

```
  [Max](#cfn-ec2-ec2fleet-acceleratortotalmemorymibrequest-max): Integer
  [Min](#cfn-ec2-ec2fleet-acceleratortotalmemorymibrequest-min): Integer
```

## Properties<a name="aws-properties-ec2-ec2fleet-acceleratortotalmemorymibrequest-properties"></a>

`Max`  <a name="cfn-ec2-ec2fleet-acceleratortotalmemorymibrequest-max"></a>
The maximum amount of accelerator memory, in MiB\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Min`  <a name="cfn-ec2-ec2fleet-acceleratortotalmemorymibrequest-min"></a>
The minimum amount of accelerator memory, in MiB\. To specify no minimum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)