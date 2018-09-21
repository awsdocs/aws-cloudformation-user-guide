# AWS OpsWorks Stack ElasticIp<a name="aws-properties-opsworks-stack-elasticip"></a>

`ElasticIps` is a property of the [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md) resource that registers an Elastic IP address with an AWS OpsWorks stack\.

## Syntax<a name="aws-properties-opsworks-stack-elasticip-syntax"></a>

### JSON<a name="aws-properties-opsworks-stack-elasticip-syntax.json"></a>

```
{
  "[Ip](#cfn-opsworks-stack-elasticip-ip)" : String,
  "[Name](#cfn-opsworks-stack-elasticip-name)" : String
}
```

### YAML<a name="aws-properties-opsworks-stack-elasticip-syntax.yaml"></a>

```
[Ip](#cfn-opsworks-stack-elasticip-ip): String
[Name](#cfn-opsworks-stack-elasticip-name): String
```

## Properties<a name="aws-properties-opsworks-stack-elasticip-properties"></a>

`Ip`  <a name="cfn-opsworks-stack-elasticip-ip"></a>
The Elastic IP address\.  
*Required*: Yes  
*Type*: String

`Name`  <a name="cfn-opsworks-stack-elasticip-name"></a>
A name for the Elastic IP address\.  
*Required*: No  
*Type*: String