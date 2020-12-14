# AWS::NetworkFirewall::FirewallPolicy StatelessRuleGroupReferences<a name="aws-properties-networkfirewall-firewallpolicy-statelessrulegroupreferences"></a>

References to the stateless rule groups that are used in the policy\. These define the matching criteria in stateless rules\. 

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-statelessrulegroupreferences-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-statelessrulegroupreferences-syntax.json"></a>

```
{
  "[StatelessRuleGroupReferences](#cfn-networkfirewall-firewallpolicy-statelessrulegroupreferences-statelessrulegroupreferences)" : [ StatelessRuleGroupReference, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-statelessrulegroupreferences-syntax.yaml"></a>

```
  [StatelessRuleGroupReferences](#cfn-networkfirewall-firewallpolicy-statelessrulegroupreferences-statelessrulegroupreferences): 
    - StatelessRuleGroupReference
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-statelessrulegroupreferences-properties"></a>

`StatelessRuleGroupReferences`  <a name="cfn-networkfirewall-firewallpolicy-statelessrulegroupreferences-statelessrulegroupreferences"></a>
References to the stateless rule groups that are used in the policy\. These define the matching criteria in stateless rules\.   
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-firewallpolicy-statelessrulegroupreferences) of [StatelessRuleGroupReference](aws-properties-networkfirewall-firewallpolicy-statelessrulegroupreference.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)