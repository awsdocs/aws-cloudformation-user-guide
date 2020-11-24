# AWS::NetworkFirewall::FirewallPolicy StatelessActions<a name="aws-properties-networkfirewall-firewallpolicy-statelessactions"></a>

The actions to take on a packet if it doesn't match any of the stateless rules in the policy\. If you want non\-matching packets to be forwarded for stateful inspection, specify `aws:forward_to_sfe`\. 

You must specify one of the standard actions: `aws:pass`, `aws:drop`, or `aws:forward_to_sfe`\. In addition, you can specify custom actions that are compatible with your standard section choice\.

For example, you could specify `["aws:pass"]` or you could specify `["aws:pass", “customActionName”]`\. For information about compatibility, see the custom action descriptions\.

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-statelessactions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-statelessactions-syntax.json"></a>

```
{
  "[StatelessActions](#cfn-networkfirewall-firewallpolicy-statelessactions-statelessactions)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-statelessactions-syntax.yaml"></a>

```
  [StatelessActions](#cfn-networkfirewall-firewallpolicy-statelessactions-statelessactions): 
    - String
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-statelessactions-properties"></a>

`StatelessActions`  <a name="cfn-networkfirewall-firewallpolicy-statelessactions-statelessactions"></a>
The actions to take on a packet if it doesn't match any of the stateless rules in the policy\. If you want non\-matching packets to be forwarded for stateful inspection, specify `aws:forward_to_sfe`\.   
You must specify one of the standard actions: `aws:pass`, `aws:drop`, or `aws:forward_to_sfe`\. In addition, you can specify custom actions that are compatible with your standard section choice\.  
For example, you could specify `["aws:pass"]` or you could specify `["aws:pass", “customActionName”]`\. For information about compatibility, see the custom action descriptions\.  
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-firewallpolicy-statelessactions) of [String](#aws-properties-networkfirewall-firewallpolicy-statelessactions)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)