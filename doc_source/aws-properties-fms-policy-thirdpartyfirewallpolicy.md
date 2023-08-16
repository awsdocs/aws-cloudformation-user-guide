# AWS::FMS::Policy ThirdPartyFirewallPolicy<a name="aws-properties-fms-policy-thirdpartyfirewallpolicy"></a>

Configures the deployment model for the third\-party firewall\.

## Syntax<a name="aws-properties-fms-policy-thirdpartyfirewallpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fms-policy-thirdpartyfirewallpolicy-syntax.json"></a>

```
{
  "[FirewallDeploymentModel](#cfn-fms-policy-thirdpartyfirewallpolicy-firewalldeploymentmodel)" : String
}
```

### YAML<a name="aws-properties-fms-policy-thirdpartyfirewallpolicy-syntax.yaml"></a>

```
  [FirewallDeploymentModel](#cfn-fms-policy-thirdpartyfirewallpolicy-firewalldeploymentmodel): String
```

## Properties<a name="aws-properties-fms-policy-thirdpartyfirewallpolicy-properties"></a>

`FirewallDeploymentModel`  <a name="cfn-fms-policy-thirdpartyfirewallpolicy-firewalldeploymentmodel"></a>
Defines the deployment model to use for the third\-party firewall policy\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CENTRALIZED | DISTRIBUTED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)