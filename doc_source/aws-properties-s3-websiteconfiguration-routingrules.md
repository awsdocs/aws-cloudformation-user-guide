# Amazon S3 Website Configuration Routing Rules Property<a name="aws-properties-s3-websiteconfiguration-routingrules"></a>

The `RoutingRules` property is an embedded property of the [Amazon S3 Website Configuration Property](aws-properties-s3-websiteconfiguration.md) property\. This property describes the redirect behavior and when a redirect is applied\.

## Syntax<a name="w3ab2c21c14e1558b5"></a>

### JSON<a name="aws-properties-s3-websiteconfiguration-routingrules-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-routingrules-redirectrule)" : Redirect rule,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition)" : Routing rule condition
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-routingrules-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-routingrules-redirectrule):
  Redirect rule
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition):
  Routing rule condition
```

## Properties<a name="w3ab2c21c14e1558b7"></a>

`RedirectRule`  
Redirect requests to another host, to another page, or with another protocol\.  
*Required: *Yes  
*Type*: [Amazon S3 Website Configuration Routing Rules Redirect Rule Property](aws-properties-s3-websiteconfiguration-routingrules-redirectrule.md)

`RoutingRuleCondition`  
Rules that define when a redirect is applied\.  
*Required: *No  
*Type*: [Amazon S3 Website Configuration Routing Rules Routing Rule Condition Property](aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition.md)