# Amazon EC2 LaunchTemplate InstanceMarketOptions<a name="aws-properties-ec2-launchtemplate-instancemarketoptions"></a>

<a name="aws-properties-ec2-launchtemplate-instancemarketoptions-description"></a>The `InstanceMarketOptions` property type specifies market \(purchasing\) option for instances in an Amazon EC2 launch template\.

<a name="aws-properties-ec2-launchtemplate-instancemarketoptions-inheritance"></a> `InstanceMarketOptions` is a property of the [Amazon EC2 LaunchTemplate LaunchTemplateData](aws-properties-ec2-launchtemplate-launchtemplatedata.md) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-instancemarketoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-instancemarketoptions-syntax.json"></a>

```
{
  "[SpotOptions](#cfn-ec2-launchtemplate-instancemarketoptions-spotoptions)" : [*SpotOptions*](aws-properties-ec2-launchtemplate-spotoptions.md),
  "[MarketType](#cfn-ec2-launchtemplate-instancemarketoptions-markettype)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-instancemarketoptions-syntax.yaml"></a>

```
[SpotOptions](#cfn-ec2-launchtemplate-instancemarketoptions-spotoptions): [*SpotOptions*](aws-properties-ec2-launchtemplate-spotoptions.md)
[MarketType](#cfn-ec2-launchtemplate-instancemarketoptions-markettype): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-instancemarketoptions-properties"></a>

`MarketType`  <a name="cfn-ec2-launchtemplate-instancemarketoptions-markettype"></a>
The market type\.  
Valid values include: `spot`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SpotOptions`  <a name="cfn-ec2-launchtemplate-instancemarketoptions-spotoptions"></a>
The options for Spot Instances\.  
 *Required*: No  
 *Type*: [Amazon EC2 LaunchTemplate SpotOptions](aws-properties-ec2-launchtemplate-spotoptions.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-launchtemplate-instancemarketoptions-seealso"></a>
+ [LaunchTemplateInstanceMarketOptionsRequest](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateInstanceMarketOptionsRequest.html) in the *Amazon EC2 API Reference*