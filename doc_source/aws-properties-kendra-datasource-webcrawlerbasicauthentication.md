# AWS::Kendra::DataSource WebCrawlerBasicAuthentication<a name="aws-properties-kendra-datasource-webcrawlerbasicauthentication"></a>

Provides the configuration information to connect to websites that require basic user authentication\.

## Syntax<a name="aws-properties-kendra-datasource-webcrawlerbasicauthentication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-webcrawlerbasicauthentication-syntax.json"></a>

```
{
  "[Credentials](#cfn-kendra-datasource-webcrawlerbasicauthentication-credentials)" : String,
  "[Host](#cfn-kendra-datasource-webcrawlerbasicauthentication-host)" : String,
  "[Port](#cfn-kendra-datasource-webcrawlerbasicauthentication-port)" : Integer
}
```

### YAML<a name="aws-properties-kendra-datasource-webcrawlerbasicauthentication-syntax.yaml"></a>

```
  [Credentials](#cfn-kendra-datasource-webcrawlerbasicauthentication-credentials): String
  [Host](#cfn-kendra-datasource-webcrawlerbasicauthentication-host): String
  [Port](#cfn-kendra-datasource-webcrawlerbasicauthentication-port): Integer
```

## Properties<a name="aws-properties-kendra-datasource-webcrawlerbasicauthentication-properties"></a>

`Credentials`  <a name="cfn-kendra-datasource-webcrawlerbasicauthentication-credentials"></a>
Your secret ARN, which you can create in [AWS Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html)   
You use a secret if basic authentication credentials are required to connect to a website\. The secret stores your credentials of user name and password\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1284`  
*Pattern*: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Host`  <a name="cfn-kendra-datasource-webcrawlerbasicauthentication-host"></a>
The name of the website host you want to connect to using authentication credentials\.  
For example, the host name of https://a\.example\.com/page1\.html is "a\.example\.com"\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `253`  
*Pattern*: `([^\s]*)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-kendra-datasource-webcrawlerbasicauthentication-port"></a>
The port number of the website host you want to connect to using authentication credentials\.  
For example, the port for https://a\.example\.com/page1\.html is 443, the standard port for HTTPS\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)