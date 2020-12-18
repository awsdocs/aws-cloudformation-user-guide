# AWS::NetworkFirewall::FirewallPolicy Dimension<a name="aws-properties-networkfirewall-firewallpolicy-dimension"></a>

The value to use in an Amazon CloudWatch custom metric dimension\. This is used in the `PublishMetrics` custom action\. A CloudWatch custom metric dimension is a name/value pair that's part of the identity of a metric\. 

AWS Network Firewall sets the dimension name to `CustomAction` and you provide the dimension value\. 

For more information about CloudWatch custom metric dimensions, see [Publishing Custom Metrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/publishingMetrics.html#usingDimensions) in the [Amazon CloudWatch User Guide](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html)\.

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-dimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-dimension-syntax.json"></a>

```
{
  "[Value](#cfn-networkfirewall-firewallpolicy-dimension-value)" : String
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-dimension-syntax.yaml"></a>

```
  [Value](#cfn-networkfirewall-firewallpolicy-dimension-value): String
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-dimension-properties"></a>

`Value`  <a name="cfn-networkfirewall-firewallpolicy-dimension-value"></a>
The value to use in the custom metric dimension\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9-_ ]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)