# AWS::EC2::EC2Fleet MemoryMiBRequest<a name="aws-properties-ec2-ec2fleet-memorymibrequest"></a>

The minimum and maximum amount of memory, in MiB\.

## Syntax<a name="aws-properties-ec2-ec2fleet-memorymibrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-memorymibrequest-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-ec2fleet-memorymibrequest-max)" : Integer,
  "[Min](#cfn-ec2-ec2fleet-memorymibrequest-min)" : Integer
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-memorymibrequest-syntax.yaml"></a>

```
  [Max](#cfn-ec2-ec2fleet-memorymibrequest-max): Integer
  [Min](#cfn-ec2-ec2fleet-memorymibrequest-min): Integer
```

## Properties<a name="aws-properties-ec2-ec2fleet-memorymibrequest-properties"></a>

`Max`  <a name="cfn-ec2-ec2fleet-memorymibrequest-max"></a>
The maximum amount of memory, in MiB\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Min`  <a name="cfn-ec2-ec2fleet-memorymibrequest-min"></a>
The minimum amount of memory, in MiB\. To specify no minimum limit, specify `0`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)