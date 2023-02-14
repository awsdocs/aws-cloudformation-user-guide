# AWS::WAFv2::WebACL ImmunityTimeProperty<a name="aws-properties-wafv2-webacl-immunitytimeproperty"></a>

Determines how long a `CAPTCHA` token remains valid after the client successfully solves a `CAPTCHA` puzzle\. 

## Syntax<a name="aws-properties-wafv2-webacl-immunitytimeproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-immunitytimeproperty-syntax.json"></a>

```
{
  "[ImmunityTime](#cfn-wafv2-webacl-immunitytimeproperty-immunitytime)" : Integer
}
```

### YAML<a name="aws-properties-wafv2-webacl-immunitytimeproperty-syntax.yaml"></a>

```
  [ImmunityTime](#cfn-wafv2-webacl-immunitytimeproperty-immunitytime): Integer
```

## Properties<a name="aws-properties-wafv2-webacl-immunitytimeproperty-properties"></a>

`ImmunityTime`  <a name="cfn-wafv2-webacl-immunitytimeproperty-immunitytime"></a>
The amount of time, in seconds, that a `CAPTCHA` token is valid\. The default setting is 300\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)