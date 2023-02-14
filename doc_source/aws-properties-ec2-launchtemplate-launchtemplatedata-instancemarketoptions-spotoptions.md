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
Deprecated\.  
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
The maximum hourly price you're willing to pay for the Spot Instances\. We do not recommend using this parameter because it can lead to increased interruptions\. If you do not specify this parameter, you will pay the current Spot price\.  
If you specify a maximum price, your Spot Instances will be interrupted more frequently than if you do not specify this parameter\.
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
The end date of the request, in UTC format \(*YYYY\-MM\-DD*T*HH:MM:SS*Z\)\. Supported only for persistent requests\.  
+ For a persistent request, the request remains active until the `ValidUntil` date and time is reached\. Otherwise, the request remains active until you cancel it\.
+ For a one\-time request, `ValidUntil` is not supported\. The request remains active until all instances launch or you cancel the request\.
Default: 7 days from the current date  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions--seealso"></a>
+  [ LaunchTemplateSpotMarketOptionsRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateSpotMarketOptionsRequest.html) in the *Amazon EC2 API Reference* 

