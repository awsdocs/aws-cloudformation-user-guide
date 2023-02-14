# AWS::EC2::SpotFleet AcceleratorCountRequest<a name="aws-properties-ec2-spotfleet-acceleratorcountrequest"></a>

The minimum and maximum number of accelerators \(GPUs, FPGAs, or AWS Inferentia chips\) on an instance\. To exclude accelerator\-enabled instance types, set `Max` to `0`\.

## Syntax<a name="aws-properties-ec2-spotfleet-acceleratorcountrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-acceleratorcountrequest-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-spotfleet-acceleratorcountrequest-max)" : Integer,
  "[Min](#cfn-ec2-spotfleet-acceleratorcountrequest-min)" : Integer
}
```

### YAML<a name="aws-properties-ec2-spotfleet-acceleratorcountrequest-syntax.yaml"></a>

```
  [Max](#cfn-ec2-spotfleet-acceleratorcountrequest-max): Integer
  [Min](#cfn-ec2-spotfleet-acceleratorcountrequest-min): Integer
```

## Properties<a name="aws-properties-ec2-spotfleet-acceleratorcountrequest-properties"></a>

`Max`  <a name="cfn-ec2-spotfleet-acceleratorcountrequest-max"></a>
The maximum number of accelerators\. To specify no maximum limit, omit this parameter\. To exclude accelerator\-enabled instance types, set `Max` to `0`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Min`  <a name="cfn-ec2-spotfleet-acceleratorcountrequest-min"></a>
The minimum number of accelerators\. To specify no minimum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)