# AWS::Shield::Protection ApplicationLayerAutomaticResponseConfiguration<a name="aws-properties-shield-protection-applicationlayerautomaticresponseconfiguration"></a>

The automatic application layer DDoS mitigation settings for a [AWS::Shield::Protection](aws-resource-shield-protection.md)\. This configuration determines whether Shield Advanced automatically manages rules in the web ACL in order to respond to application layer events that Shield Advanced determines to be DDoS attacks\. 

## Syntax<a name="aws-properties-shield-protection-applicationlayerautomaticresponseconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-shield-protection-applicationlayerautomaticresponseconfiguration-syntax.json"></a>

```
{
  "[Action](#cfn-shield-protection-applicationlayerautomaticresponseconfiguration-action)" : Action,
  "[Status](#cfn-shield-protection-applicationlayerautomaticresponseconfiguration-status)" : String
}
```

### YAML<a name="aws-properties-shield-protection-applicationlayerautomaticresponseconfiguration-syntax.yaml"></a>

```
  [Action](#cfn-shield-protection-applicationlayerautomaticresponseconfiguration-action): 
    Action
  [Status](#cfn-shield-protection-applicationlayerautomaticresponseconfiguration-status): String
```

## Properties<a name="aws-properties-shield-protection-applicationlayerautomaticresponseconfiguration-properties"></a>

`Action`  <a name="cfn-shield-protection-applicationlayerautomaticresponseconfiguration-action"></a>
Specifies the action setting that Shield Advanced should use in the AWS WAF rules that it creates on behalf of the protected resource in response to DDoS attacks\. You specify this as part of the configuration for the automatic application layer DDoS mitigation feature, when you enable or update automatic mitigation\. Shield Advanced creates the AWS WAF rules in a Shield Advanced\-managed rule group, inside the web ACL that you have associated with the resource\.   
*Required*: Yes  
*Type*: [Action](aws-properties-shield-protection-action.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-shield-protection-applicationlayerautomaticresponseconfiguration-status"></a>
Indicates whether automatic application layer DDoS mitigation is enabled for the protection\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)