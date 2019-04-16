# Amazon S3 Bucket RoutingRules<a name="aws-properties-s3-websiteconfiguration-routingrules"></a>

The `RoutingRules` property is an embedded property of the [WebsiteConfiguration](aws-properties-s3-websiteconfiguration.md) property\. This property describes the redirect behavior and when a redirect is applied\.

## Syntax<a name="w13ab1c21c10d204c13d130b5"></a>

### JSON<a name="aws-properties-s3-websiteconfiguration-routingrules-syntax.json"></a>

```
{
  "[RedirectRule](#cfn-s3-websiteconfiguration-routingrules-redirectrule)" : Redirect rule,
  "[RoutingRuleCondition](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition)" : Routing rule condition
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-routingrules-syntax.yaml"></a>

```
[RedirectRule](#cfn-s3-websiteconfiguration-routingrules-redirectrule):
  Redirect rule
[RoutingRuleCondition](#cfn-s3-websiteconfiguration-routingrules-routingrulecondition):
  Routing rule condition
```

## Properties<a name="w13ab1c21c10d204c13d130b7"></a>

`RedirectRule`  <a name="cfn-s3-websiteconfiguration-routingrules-redirectrule"></a>
Redirect requests to another host, to another page, or with another protocol\.  
*Required*: Yes  
*Type*: [RedirectRule](aws-properties-s3-websiteconfiguration-routingrules-redirectrule.md)

`RoutingRuleCondition`  <a name="cfn-s3-websiteconfiguration-routingrules-routingrulecondition"></a>
Rules that define when a redirect is applied\.  
*Required*: No  
*Type*: [RoutingRuleCondition](aws-properties-s3-websiteconfiguration-routingrules-routingrulecondition.md)