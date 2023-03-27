# AWS::WAFv2::RuleGroup ChallengeConfig<a name="aws-properties-wafv2-rulegroup-challengeconfig"></a>

Specifies how AWS WAF should handle `Challenge` evaluations\. This is available at the web ACL level and in each rule\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-challengeconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-challengeconfig-syntax.json"></a>

```
{
  "[ImmunityTimeProperty](#cfn-wafv2-rulegroup-challengeconfig-immunitytimeproperty)" : ImmunityTimeProperty
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-challengeconfig-syntax.yaml"></a>

```
  [ImmunityTimeProperty](#cfn-wafv2-rulegroup-challengeconfig-immunitytimeproperty): 
    ImmunityTimeProperty
```

## Properties<a name="aws-properties-wafv2-rulegroup-challengeconfig-properties"></a>

`ImmunityTimeProperty`  <a name="cfn-wafv2-rulegroup-challengeconfig-immunitytimeproperty"></a>
Determines how long a challenge timestamp in the token remains valid after the client successfully responds to a challenge\.   
*Required*: No  
*Type*: [ImmunityTimeProperty](aws-properties-wafv2-rulegroup-immunitytimeproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)