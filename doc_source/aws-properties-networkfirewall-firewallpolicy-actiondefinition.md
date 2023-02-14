# AWS::NetworkFirewall::FirewallPolicy ActionDefinition<a name="aws-properties-networkfirewall-firewallpolicy-actiondefinition"></a>

A custom action to use in stateless rule actions settings\. 

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-actiondefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-actiondefinition-syntax.json"></a>

```
{
  "[PublishMetricAction](#cfn-networkfirewall-firewallpolicy-actiondefinition-publishmetricaction)" : PublishMetricAction
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-actiondefinition-syntax.yaml"></a>

```
  [PublishMetricAction](#cfn-networkfirewall-firewallpolicy-actiondefinition-publishmetricaction): 
    PublishMetricAction
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-actiondefinition-properties"></a>

`PublishMetricAction`  <a name="cfn-networkfirewall-firewallpolicy-actiondefinition-publishmetricaction"></a>
Stateless inspection criteria that publishes the specified metrics to Amazon CloudWatch for the matching packet\. This setting defines a CloudWatch dimension value to be published\.  
You can pair this custom action with any of the standard stateless rule actions\. For example, you could pair this in a rule action with the standard action that forwards the packet for stateful inspection\. Then, when a packet matches the rule, Network Firewall publishes metrics for the packet and forwards it\.   
*Required*: No  
*Type*: [PublishMetricAction](aws-properties-networkfirewall-firewallpolicy-publishmetricaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)