# AWS::Kendra::DataSource WebCrawlerAuthenticationConfiguration<a name="aws-properties-kendra-datasource-webcrawlerauthenticationconfiguration"></a>

Provides the configuration information to connect to websites that require user authentication\.

## Syntax<a name="aws-properties-kendra-datasource-webcrawlerauthenticationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-webcrawlerauthenticationconfiguration-syntax.json"></a>

```
{
  "[BasicAuthentication](#cfn-kendra-datasource-webcrawlerauthenticationconfiguration-basicauthentication)" : [ WebCrawlerBasicAuthentication, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-webcrawlerauthenticationconfiguration-syntax.yaml"></a>

```
  [BasicAuthentication](#cfn-kendra-datasource-webcrawlerauthenticationconfiguration-basicauthentication): 
    - WebCrawlerBasicAuthentication
```

## Properties<a name="aws-properties-kendra-datasource-webcrawlerauthenticationconfiguration-properties"></a>

`BasicAuthentication`  <a name="cfn-kendra-datasource-webcrawlerauthenticationconfiguration-basicauthentication"></a>
The list of configuration information that's required to connect to and crawl a website host using basic authentication credentials\.  
The list includes the name and port number of the website host\.  
*Required*: No  
*Type*: List of [WebCrawlerBasicAuthentication](aws-properties-kendra-datasource-webcrawlerbasicauthentication.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)