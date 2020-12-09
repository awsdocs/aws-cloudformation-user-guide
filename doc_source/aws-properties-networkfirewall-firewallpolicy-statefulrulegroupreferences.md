# AWS::NetworkFirewall::FirewallPolicy StatefulRuleGroupReferences<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreferences"></a>

References to the stateless rule groups that are used in the policy\. These define the inspection criteria in stateful rules\. 

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreferences-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreferences-syntax.json"></a>

```
{
  "[StatefulRuleGroupReferences](#cfn-networkfirewall-firewallpolicy-statefulrulegroupreferences-statefulrulegroupreferences)" : [ StatefulRuleGroupReference, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreferences-syntax.yaml"></a>

```
  [StatefulRuleGroupReferences](#cfn-networkfirewall-firewallpolicy-statefulrulegroupreferences-statefulrulegroupreferences): 
    - StatefulRuleGroupReference
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreferences-properties"></a>

`StatefulRuleGroupReferences`  <a name="cfn-networkfirewall-firewallpolicy-statefulrulegroupreferences-statefulrulegroupreferences"></a>
References to the stateless rule groups that are used in the policy\. These define the inspection criteria in stateful rules\.   
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreferences) of [StatefulRuleGroupReference](aws-properties-networkfirewall-firewallpolicy-statefulrulegroupreference.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)