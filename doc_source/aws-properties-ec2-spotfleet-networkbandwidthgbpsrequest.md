# AWS::EC2::SpotFleet NetworkBandwidthGbpsRequest<a name="aws-properties-ec2-spotfleet-networkbandwidthgbpsrequest"></a>

The minimum and maximum amount of baseline network bandwidth, in gigabits per second \(Gbps\)\. For more information, see [Amazon EC2 instance network bandwidth](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-network-bandwidth.html) in the *Amazon EC2 User Guide*\.

Default: No minimum or maximum limits

## Syntax<a name="aws-properties-ec2-spotfleet-networkbandwidthgbpsrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-networkbandwidthgbpsrequest-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-spotfleet-networkbandwidthgbpsrequest-max)" : Double,
  "[Min](#cfn-ec2-spotfleet-networkbandwidthgbpsrequest-min)" : Double
}
```

### YAML<a name="aws-properties-ec2-spotfleet-networkbandwidthgbpsrequest-syntax.yaml"></a>

```
  [Max](#cfn-ec2-spotfleet-networkbandwidthgbpsrequest-max): Double
  [Min](#cfn-ec2-spotfleet-networkbandwidthgbpsrequest-min): Double
```

## Properties<a name="aws-properties-ec2-spotfleet-networkbandwidthgbpsrequest-properties"></a>

`Max`  <a name="cfn-ec2-spotfleet-networkbandwidthgbpsrequest-max"></a>
The maximum amount of network bandwidth, in Gbps\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Min`  <a name="cfn-ec2-spotfleet-networkbandwidthgbpsrequest-min"></a>
The minimum amount of network bandwidth, in Gbps\. To specify no minimum limit, omit this parameter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)