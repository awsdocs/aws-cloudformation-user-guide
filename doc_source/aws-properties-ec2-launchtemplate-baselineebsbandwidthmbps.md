# AWS::EC2::LaunchTemplate BaselineEbsBandwidthMbps<a name="aws-properties-ec2-launchtemplate-baselineebsbandwidthmbps"></a>

The minimum and maximum baseline bandwidth to Amazon EBS, in Mbps\. For more information, see [Amazon EBS–optimized instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-optimized.html) in the *Amazon EC2 User Guide*\.

## Syntax<a name="aws-properties-ec2-launchtemplate-baselineebsbandwidthmbps-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-baselineebsbandwidthmbps-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-launchtemplate-baselineebsbandwidthmbps-max)" : Integer,
  "[Min](#cfn-ec2-launchtemplate-baselineebsbandwidthmbps-min)" : Integer
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-baselineebsbandwidthmbps-syntax.yaml"></a>

```
  [Max](#cfn-ec2-launchtemplate-baselineebsbandwidthmbps-max): Integer
  [Min](#cfn-ec2-launchtemplate-baselineebsbandwidthmbps-min): Integer
```

## Properties<a name="aws-properties-ec2-launchtemplate-baselineebsbandwidthmbps-properties"></a>

`Max`  <a name="cfn-ec2-launchtemplate-baselineebsbandwidthmbps-max"></a>
The maximum baseline bandwidth, in Mbps\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-ec2-launchtemplate-baselineebsbandwidthmbps-min"></a>
The minimum baseline bandwidth, in Mbps\. To specify no minimum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)