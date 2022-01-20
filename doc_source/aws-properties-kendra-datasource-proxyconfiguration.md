# AWS::Kendra::DataSource ProxyConfiguration<a name="aws-properties-kendra-datasource-proxyconfiguration"></a>

Provides the configuration information for a web proxy to connect to website hosts\.

## Syntax<a name="aws-properties-kendra-datasource-proxyconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-proxyconfiguration-syntax.json"></a>

```
{
  "[Credentials](#cfn-kendra-datasource-proxyconfiguration-credentials)" : String,
  "[Host](#cfn-kendra-datasource-proxyconfiguration-host)" : String,
  "[Port](#cfn-kendra-datasource-proxyconfiguration-port)" : Integer
}
```

### YAML<a name="aws-properties-kendra-datasource-proxyconfiguration-syntax.yaml"></a>

```
  [Credentials](#cfn-kendra-datasource-proxyconfiguration-credentials): String
  [Host](#cfn-kendra-datasource-proxyconfiguration-host): String
  [Port](#cfn-kendra-datasource-proxyconfiguration-port): Integer
```

## Properties<a name="aws-properties-kendra-datasource-proxyconfiguration-properties"></a>

`Credentials`  <a name="cfn-kendra-datasource-proxyconfiguration-credentials"></a>
Your secret ARN, which you can create in [AWS Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html)   
The credentials are optional\. You use a secret if web proxy credentials are required to connect to a website host\. Amazon Kendra currently support basic authentication to connect to a web proxy server\. The secret stores your credentials\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1284`  
*Pattern*: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Host`  <a name="cfn-kendra-datasource-proxyconfiguration-host"></a>
The name of the website host you want to connect to via a web proxy server\.  
For example, the host name of https://a\.example\.com/page1\.html is "a\.example\.com"\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `253`  
*Pattern*: `([^\s]*)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-kendra-datasource-proxyconfiguration-port"></a>
The port number of the website host you want to connect to via a web proxy server\.   
For example, the port for https://a\.example\.com/page1\.html is 443, the standard port for HTTPS\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)