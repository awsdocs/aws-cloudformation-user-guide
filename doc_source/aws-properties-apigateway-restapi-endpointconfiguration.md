# Amazon API Gateway RestApi EndpointConfiguration<a name="aws-properties-apigateway-restapi-endpointconfiguration"></a>

<a name="aws-properties-apigateway-restapi-endpointconfiguration-description"></a>The `EndpointConfiguration` property type specifies the endpoint types of an Amazon API Gateway REST API\.

<a name="aws-properties-apigateway-restapi-endpointconfiguration-inheritance"></a> `EndpointConfiguration` is a property of the [AWS::ApiGateway::RestApi](aws-resource-apigateway-restapi.md) resource\.

## Syntax<a name="aws-properties-apigateway-restapi-endpointconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-restapi-endpointconfiguration-syntax.json"></a>

```
{
  "[Types](#cfn-apigateway-restapi-endpointconfiguration-types)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-apigateway-restapi-endpointconfiguration-syntax.yaml"></a>

```
[Types](#cfn-apigateway-restapi-endpointconfiguration-types): 
  - String
```

## Properties<a name="aws-properties-apigateway-restapi-endpointconfiguration-properties"></a>

`Types`  <a name="cfn-apigateway-restapi-endpointconfiguration-types"></a>
A list of endpoint types of an API or its custom domain name\. Valid values include:  
+ `EDGE`: For an edge\-optimized API and its custom domain name\.
+ `REGIONAL`: For a regional API and its custom domain name\.
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-apigateway-restapi-endpointconfiguration-seealso"></a>
+ [endpointConfiguration](http://docs.aws.amazon.com/apigateway/api-reference/link-relation/restapi-create/#endpointConfiguration) in the *API Gateway API Reference*