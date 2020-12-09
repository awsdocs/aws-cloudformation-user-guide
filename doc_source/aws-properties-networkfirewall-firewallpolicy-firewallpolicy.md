# AWS::NetworkFirewall::FirewallPolicy FirewallPolicy<a name="aws-properties-networkfirewall-firewallpolicy-firewallpolicy"></a>

The traffic filtering behavior of a firewall policy, defined in a collection of stateless and stateful rule groups and other settings\. 

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-firewallpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-firewallpolicy-syntax.json"></a>

```
{
  "[StatefulRuleGroupReferences](#cfn-networkfirewall-firewallpolicy-firewallpolicy-statefulrulegroupreferences)" : StatefulRuleGroupReferences,
  "[StatelessCustomActions](#cfn-networkfirewall-firewallpolicy-firewallpolicy-statelesscustomactions)" : CustomActions,
  "[StatelessDefaultActions](#cfn-networkfirewall-firewallpolicy-firewallpolicy-statelessdefaultactions)" : StatelessActions,
  "[StatelessFragmentDefaultActions](#cfn-networkfirewall-firewallpolicy-firewallpolicy-statelessfragmentdefaultactions)" : StatelessActions,
  "[StatelessRuleGroupReferences](#cfn-networkfirewall-firewallpolicy-firewallpolicy-statelessrulegroupreferences)" : StatelessRuleGroupReferences
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-firewallpolicy-syntax.yaml"></a>

```
  [StatefulRuleGroupReferences](#cfn-networkfirewall-firewallpolicy-firewallpolicy-statefulrulegroupreferences): 
    StatefulRuleGroupReferences
  [StatelessCustomActions](#cfn-networkfirewall-firewallpolicy-firewallpolicy-statelesscustomactions): 
    CustomActions
  [StatelessDefaultActions](#cfn-networkfirewall-firewallpolicy-firewallpolicy-statelessdefaultactions): 
    StatelessActions
  [StatelessFragmentDefaultActions](#cfn-networkfirewall-firewallpolicy-firewallpolicy-statelessfragmentdefaultactions): 
    StatelessActions
  [StatelessRuleGroupReferences](#cfn-networkfirewall-firewallpolicy-firewallpolicy-statelessrulegroupreferences): 
    StatelessRuleGroupReferences
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-firewallpolicy-properties"></a>

`StatefulRuleGroupReferences`  <a name="cfn-networkfirewall-firewallpolicy-firewallpolicy-statefulrulegroupreferences"></a>
References to the stateless rule groups that are used in the policy\. These define the inspection criteria in stateful rules\.   
*Required*: No  
*Type*: [StatefulRuleGroupReferences](aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreferences.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatelessCustomActions`  <a name="cfn-networkfirewall-firewallpolicy-firewallpolicy-statelesscustomactions"></a>
The custom action definitions that are available for use in the firewall policy's `StatelessDefaultActions` setting\. You name each custom action that you define, and then you can use it by name in your default actions specifications\.  
*Required*: No  
*Type*: [CustomActions](aws-properties-networkfirewall-firewallpolicy-customactions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatelessDefaultActions`  <a name="cfn-networkfirewall-firewallpolicy-firewallpolicy-statelessdefaultactions"></a>
The actions to take on a packet if it doesn't match any of the stateless rules in the policy\. If you want non\-matching packets to be forwarded for stateful inspection, specify `aws:forward_to_sfe`\.   
You must specify one of the standard actions: `aws:pass`, `aws:drop`, or `aws:forward_to_sfe`\. In addition, you can specify custom actions that are compatible with your standard section choice\.  
For example, you could specify `["aws:pass"]` or you could specify `["aws:pass", “customActionName”]`\. For information about compatibility, see the custom action descriptions\.  
*Required*: Yes  
*Type*: [StatelessActions](aws-properties-networkfirewall-firewallpolicy-statelessactions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatelessFragmentDefaultActions`  <a name="cfn-networkfirewall-firewallpolicy-firewallpolicy-statelessfragmentdefaultactions"></a>
The actions to take on a fragmented packet if it doesn't match any of the stateless rules in the policy\. If you want non\-matching fragmented packets to be forwarded for stateful inspection, specify `aws:forward_to_sfe`\.   
You must specify one of the standard actions: `aws:pass`, `aws:drop`, or `aws:forward_to_sfe`\. In addition, you can specify custom actions that are compatible with your standard section choice\.  
For example, you could specify `["aws:pass"]` or you could specify `["aws:pass", “customActionName”]`\. For information about compatibility, see the custom action descriptions\.  
*Required*: Yes  
*Type*: [StatelessActions](aws-properties-networkfirewall-firewallpolicy-statelessactions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatelessRuleGroupReferences`  <a name="cfn-networkfirewall-firewallpolicy-firewallpolicy-statelessrulegroupreferences"></a>
References to the stateless rule groups that are used in the policy\. These define the matching criteria in stateless rules\.   
*Required*: No  
*Type*: [StatelessRuleGroupReferences](aws-properties-networkfirewall-firewallpolicy-statelessrulegroupreferences.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)