# Amazon Route 53 HostedZoneTags<a name="aws-properties-route53-hostedzone-hostedzonetags"></a>

The `HostedZoneTags` property describes key\-value pairs that are associated with an [AWS::Route53::HostedZone](aws-resource-route53-hostedzone.md) resource\.

## Syntax<a name="w3ab2c21c14e1665b5"></a>

### JSON<a name="aws-properties-route53-hostedzone-hostedzonetags-syntax.json"></a>

```
{
  "[Key](#cfn-route53-hostedzonetags-key)" : String,
  "[Value](#cfn-route53-hostedzonetags-value)" : String
}
```

### YAML<a name="aws-properties-route53-hostedzone-hostedzonetags-syntax.yaml"></a>

```
[Key](#cfn-route53-hostedzonetags-key): String
[Value](#cfn-route53-hostedzonetags-value): String
```

## Properties<a name="w3ab2c21c14e1665b7"></a>

`Key`  <a name="cfn-route53-hostedzonetags-key"></a>
The key name of the tag\.  
*Required*: Yes  
*Type*: String

`Value`  <a name="cfn-route53-hostedzonetags-value"></a>
The value for the tag\.  
*Required*: Yes  
*Type*: String