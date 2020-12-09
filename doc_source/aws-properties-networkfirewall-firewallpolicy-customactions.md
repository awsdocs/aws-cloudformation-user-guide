# AWS::NetworkFirewall::FirewallPolicy CustomActions<a name="aws-properties-networkfirewall-firewallpolicy-customactions"></a>

Optional, non\-standard actions to use for stateless packet handling\. You can define these in addition to the standard action that you must specify\. 

You define and name the custom actions that you want to be able to use, and then you reference them by name in your actions settings\. 

## Syntax<a name="aws-properties-networkfirewall-firewallpolicy-customactions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-firewallpolicy-customactions-syntax.json"></a>

```
{
  "[CustomActions](#cfn-networkfirewall-firewallpolicy-customactions-customactions)" : [ CustomAction, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-firewallpolicy-customactions-syntax.yaml"></a>

```
  [CustomActions](#cfn-networkfirewall-firewallpolicy-customactions-customactions): 
    - CustomAction
```

## Properties<a name="aws-properties-networkfirewall-firewallpolicy-customactions-properties"></a>

`CustomActions`  <a name="cfn-networkfirewall-firewallpolicy-customactions-customactions"></a>
Optional, non\-standard actions to use for stateless packet handling\. You can define these in your rule actions, in addition to the standard action that you must specify\.   
You define and name the custom actions that you want to be able to use, and then you reference them by name in your actions settings\.   
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-firewallpolicy-customactions) of [CustomAction](aws-properties-networkfirewall-firewallpolicy-customaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)