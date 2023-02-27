# AWS::NetworkFirewall::FirewallPolicy StatefulRuleGroupOverride<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupoverride"></a>

The setting that allows the policy owner to change the behavior of the rule group within a policy\. 

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupoverride-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupoverride-syntax.json"></a>

```
{
  "[Action](#cfn-networkfirewall-firewallpolicy-statefulrulegroupoverride-action)" : String
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupoverride-syntax.yaml"></a>

```
  [Action](#cfn-networkfirewall-firewallpolicy-statefulrulegroupoverride-action): String
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-statefulrulegroupoverride-properties"></a>

`Action`  <a name="cfn-networkfirewall-firewallpolicy-statefulrulegroupoverride-action"></a>
The action that changes the rule group from `DROP` to `ALERT`\. This only applies to managed rule groups\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DROP_TO_ALERT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)