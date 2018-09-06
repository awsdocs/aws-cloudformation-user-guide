# Amazon Route 53 HealthCheck HealthCheckTags<a name="aws-properties-route53-healthcheck-healthchecktags"></a>

The `HealthCheckTags` property describes key\-value pairs that are associated with an [AWS::Route53::HealthCheck](aws-resource-route53-healthcheck.md) resource\.

## Syntax<a name="w3ab2c21c14e1657b5"></a>

### JSON<a name="aws-properties-route53-healthcheck-healthchecktags-syntax.json"></a>

```
{
  "[Key](#cfn-route53-healthchecktags-key)" : String,
  "[Value](#cfn-route53-healthchecktags-value)" : String
}
```

### YAML<a name="aws-properties-route53-healthcheck-healthchecktags-syntax.yaml"></a>

```
[Key](#cfn-route53-healthchecktags-key): String
[Value](#cfn-route53-healthchecktags-value): String
```

## Properties<a name="w3ab2c21c14e1657b7"></a>

`Key`  <a name="cfn-route53-healthchecktags-key"></a>
The key name of the tag\.  
*Required*: Yes  
*Type*: String

`Value`  <a name="cfn-route53-healthchecktags-value"></a>
The value for the tag\.  
*Required*: Yes  
*Type*: String