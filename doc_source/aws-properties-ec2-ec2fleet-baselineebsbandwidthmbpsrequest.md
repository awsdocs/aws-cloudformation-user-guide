# AWS::EC2::EC2Fleet BaselineEbsBandwidthMbpsRequest<a name="aws-properties-ec2-ec2fleet-baselineebsbandwidthmbpsrequest"></a>

The minimum and maximum baseline bandwidth to Amazon EBS, in Mbps\. For more information, see [Amazon EBS–optimized instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-optimized.html) in the *Amazon EC2 User Guide*\.

## Syntax<a name="aws-properties-ec2-ec2fleet-baselineebsbandwidthmbpsrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-baselineebsbandwidthmbpsrequest-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-ec2fleet-baselineebsbandwidthmbpsrequest-max)" : Integer,
  "[Min](#cfn-ec2-ec2fleet-baselineebsbandwidthmbpsrequest-min)" : Integer
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-baselineebsbandwidthmbpsrequest-syntax.yaml"></a>

```
  [Max](#cfn-ec2-ec2fleet-baselineebsbandwidthmbpsrequest-max): Integer
  [Min](#cfn-ec2-ec2fleet-baselineebsbandwidthmbpsrequest-min): Integer
```

## Properties<a name="aws-properties-ec2-ec2fleet-baselineebsbandwidthmbpsrequest-properties"></a>

`Max`  <a name="cfn-ec2-ec2fleet-baselineebsbandwidthmbpsrequest-max"></a>
The maximum baseline bandwidth, in Mbps\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Min`  <a name="cfn-ec2-ec2fleet-baselineebsbandwidthmbpsrequest-min"></a>
The minimum baseline bandwidth, in Mbps\. To specify no minimum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)