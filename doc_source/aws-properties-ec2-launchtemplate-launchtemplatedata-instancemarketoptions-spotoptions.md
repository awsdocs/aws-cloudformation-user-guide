# AWS::EC2::LaunchTemplate SpotOptions<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions"></a>

Specifies options for Spot instances\.

 `SpotOptions` is a property of the [Amazon EC2 LaunchTemplate InstanceMarketOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-instancemarketoptions.html) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-syntax.json"></a>

```
{
  "[InstanceInterruptionBehavior](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-instanceinterruptionbehavior)" : String,
  "[MaxPrice](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-maxprice)" : String,
  "[SpotInstanceType](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-spotinstancetype)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-syntax.yaml"></a>

```
  [InstanceInterruptionBehavior](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-instanceinterruptionbehavior): String
  [MaxPrice](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-maxprice): String
  [SpotInstanceType](#cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-spotinstancetype): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-properties"></a>

`InstanceInterruptionBehavior`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-instanceinterruptionbehavior"></a>
The behavior when a Spot Instance is interrupted\. The default is `terminate`\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `hibernate | stop | terminate`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxPrice`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-maxprice"></a>
The maximum hourly price you're willing to pay for the Spot Instances\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpotInstanceType`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions-spotinstancetype"></a>
The Spot Instance request type\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `one-time | persistent`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions--seealso"></a>
+  [ LaunchTemplateSpotMarketOptionsRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateSpotMarketOptionsRequest.html) in the *Amazon Elastic Compute Cloud API Reference* 