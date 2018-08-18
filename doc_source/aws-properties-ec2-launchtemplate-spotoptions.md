# Amazon EC2 LaunchTemplate SpotOptions<a name="aws-properties-ec2-launchtemplate-spotoptions"></a>

<a name="aws-properties-ec2-launchtemplate-spotoptions-description"></a>The `SpotOptions` property type specifies the options for Spot Instances in an Amazon EC2 launch template\.

<a name="aws-properties-ec2-launchtemplate-spotoptions-inheritance"></a> `SpotOptions` is a property of the [Amazon EC2 LaunchTemplate InstanceMarketOptions](aws-properties-ec2-launchtemplate-instancemarketoptions.md) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-spotoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-spotoptions-syntax.json"></a>

```
{
  "[SpotInstanceType](#cfn-ec2-launchtemplate-spotoptions-spotinstancetype)" : String,
  "[InstanceInterruptionBehavior](#cfn-ec2-launchtemplate-spotoptions-instanceinterruptionbehavior)" : String,
  "[MaxPrice](#cfn-ec2-launchtemplate-spotoptions-maxprice)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-spotoptions-syntax.yaml"></a>

```
[SpotInstanceType](#cfn-ec2-launchtemplate-spotoptions-spotinstancetype): String
[InstanceInterruptionBehavior](#cfn-ec2-launchtemplate-spotoptions-instanceinterruptionbehavior): String
[MaxPrice](#cfn-ec2-launchtemplate-spotoptions-maxprice): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-spotoptions-properties"></a>

`InstanceInterruptionBehavior`  <a name="cfn-ec2-launchtemplate-spotoptions-instanceinterruptionbehavior"></a>
The behavior when a Spot Instance is interrupted\. The default is `terminate`\.  
Valid values include: `hibernate`, `stop`, and `terminate`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MaxPrice`  <a name="cfn-ec2-launchtemplate-spotoptions-maxprice"></a>
The maximum hourly price you're willing to pay for the Spot Instances\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SpotInstanceType`  <a name="cfn-ec2-launchtemplate-spotoptions-spotinstancetype"></a>
The Spot Instance request type\.  
Valid values include: `one-time` and `persistent`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-launchtemplate-spotoptions-seealso"></a>
+ [LaunchTemplateSpotMarketOptionsRequest](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateSpotMarketOptionsRequest.html) in the *Amazon EC2 API Reference*