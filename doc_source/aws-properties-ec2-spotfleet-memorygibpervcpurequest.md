# AWS::EC2::SpotFleet MemoryGiBPerVCpuRequest<a name="aws-properties-ec2-spotfleet-memorygibpervcpurequest"></a>

The minimum and maximum amount of memory per vCPU, in GiB\.

## Syntax<a name="aws-properties-ec2-spotfleet-memorygibpervcpurequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-memorygibpervcpurequest-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-spotfleet-memorygibpervcpurequest-max)" : Double,
  "[Min](#cfn-ec2-spotfleet-memorygibpervcpurequest-min)" : Double
}
```

### YAML<a name="aws-properties-ec2-spotfleet-memorygibpervcpurequest-syntax.yaml"></a>

```
  [Max](#cfn-ec2-spotfleet-memorygibpervcpurequest-max): Double
  [Min](#cfn-ec2-spotfleet-memorygibpervcpurequest-min): Double
```

## Properties<a name="aws-properties-ec2-spotfleet-memorygibpervcpurequest-properties"></a>

`Max`  <a name="cfn-ec2-spotfleet-memorygibpervcpurequest-max"></a>
The maximum amount of memory per vCPU, in GiB\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Min`  <a name="cfn-ec2-spotfleet-memorygibpervcpurequest-min"></a>
The minimum amount of memory per vCPU, in GiB\. To specify no minimum limit, omit this parameter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)