# AWS::EC2::LaunchTemplate SpotOptions<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions"></a>

Specifies options for Spot Instances\.

`SpotOptions` is a property of [AWS::EC2::LaunchTemplate InstanceMarketOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-syntax.json"></a>

```
{
  "[BlockDurationMinutes](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-blockdurationminutes)" : Integer,
  "[InstanceInterruptionBehavior](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-instanceinterruptionbehavior)" : String,
  "[MaxPrice](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-maxprice)" : String,
  "[SpotInstanceType](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-spotinstancetype)" : String,
  "[ValidUntil](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-validuntil)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-syntax.yaml"></a>

```
  [BlockDurationMinutes](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-blockdurationminutes): Integer
  [InstanceInterruptionBehavior](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-instanceinterruptionbehavior): String
  [MaxPrice](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-maxprice): String
  [SpotInstanceType](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-spotinstancetype): String
  [ValidUntil](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-validuntil): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-properties"></a>

`BlockDurationMinutes`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-blockdurationminutes"></a>
The required duration for the Spot Instances \(also known as Spot blocks\), in minutes\. This value must be a multiple of 60 \(60, 120, 180, 240, 300, or 360\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceInterruptionBehavior`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-instanceinterruptionbehavior"></a>
The behavior when a Spot Instance is interrupted\. The default is `terminate`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `hibernate | stop | terminate`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxPrice`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-maxprice"></a>
The maximum hourly price you're willing to pay for the Spot Instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotInstanceType`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-spotinstancetype"></a>
The Spot Instance request type\.  
If you are using Spot Instances with an Auto Scaling group, use `one-time` requests, as the Amazon EC2 Auto Scaling service handles requesting new Spot Instances whenever the group is below its desired capacity\.  
*Required*: No  
*Type*: String  
*Allowed values*: `one-time | persistent`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValidUntil`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-validuntil"></a>
The end date of the request\. For a one\-time request, the request remains active until all instances launch, the request is canceled, or this date is reached\. If the request is persistent, it remains active until it is canceled or this date and time is reached\. The default end date is 7 days from the current date\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions--seealso"></a>
+  [ LaunchTemplateSpotMarketOptionsRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateSpotMarketOptionsRequest.html) in the *Amazon Elastic Compute Cloud API Reference* 

