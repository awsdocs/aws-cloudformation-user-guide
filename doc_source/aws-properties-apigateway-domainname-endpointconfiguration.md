# AWS::ApiGateway::DomainName EndpointConfiguration<a name="aws-properties-apigateway-domainname-endpointconfiguration"></a>

The `EndpointConfiguration` property type specifies the endpoint types of an Amazon API Gateway domain name\.

`EndpointConfiguration` is a property of the [AWS::ApiGateway::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-domainname.html) resource\.

## Syntax<a name="aws-properties-apigateway-domainname-endpointconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-domainname-endpointconfiguration-syntax.json"></a>

```
{
  "[Types](#cfn-apigateway-domainname-endpointconfiguration-types)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-apigateway-domainname-endpointconfiguration-syntax.yaml"></a>

```
  [Types](#cfn-apigateway-domainname-endpointconfiguration-types): 
    - String
```

## Properties<a name="aws-properties-apigateway-domainname-endpointconfiguration-properties"></a>

`Types`  <a name="cfn-apigateway-domainname-endpointconfiguration-types"></a>
A list of endpoint types of an API or its custom domain name\. For an edge\-optimized API and its custom domain name, the endpoint type is `EDGE`\. For a regional API and its custom domain name, the endpoint type is `REGIONAL`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-domainname-endpointconfiguration--seealso"></a>
+ [DomainName](https://docs.aws.amazon.com/apigateway/api-reference/resource/domain-name/) in the *Amazon API Gateway REST API Reference*

