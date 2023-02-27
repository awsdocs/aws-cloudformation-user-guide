# AWS::FMS::Policy PolicyOption<a name="aws-properties-fms-policy-policyoption"></a>

Contains the AWS Network Firewall firewall policy options to configure the policy's deployment model and third\-party firewall policy settings\.

## Syntax<a name="aws-properties-fms-policy-policyoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fms-policy-policyoption-syntax.json"></a>

```
{
  "[NetworkFirewallPolicy](#cfn-fms-policy-policyoption-networkfirewallpolicy)" : NetworkFirewallPolicy,
  "[ThirdPartyFirewallPolicy](#cfn-fms-policy-policyoption-thirdpartyfirewallpolicy)" : ThirdPartyFirewallPolicy
}
```

### YAML<a name="aws-properties-fms-policy-policyoption-syntax.yaml"></a>

```
  [NetworkFirewallPolicy](#cfn-fms-policy-policyoption-networkfirewallpolicy): 
    NetworkFirewallPolicy
  [ThirdPartyFirewallPolicy](#cfn-fms-policy-policyoption-thirdpartyfirewallpolicy): 
    ThirdPartyFirewallPolicy
```

## Properties<a name="aws-properties-fms-policy-policyoption-properties"></a>

`NetworkFirewallPolicy`  <a name="cfn-fms-policy-policyoption-networkfirewallpolicy"></a>
Defines the deployment model to use for the firewall policy\.  
*Required*: No  
*Type*: [NetworkFirewallPolicy](aws-properties-fms-policy-networkfirewallpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThirdPartyFirewallPolicy`  <a name="cfn-fms-policy-policyoption-thirdpartyfirewallpolicy"></a>
Defines the policy options for a third\-party firewall policy\.  
*Required*: No  
*Type*: [ThirdPartyFirewallPolicy](aws-properties-fms-policy-thirdpartyfirewallpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)