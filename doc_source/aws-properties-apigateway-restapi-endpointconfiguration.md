# AWS::ApiGateway::RestApi EndpointConfiguration<a name="aws-properties-apigateway-restapi-endpointconfiguration"></a>

The `EndpointConfiguration` property type specifies the endpoint types of a REST API\.

`EndpointConfiguration` is a property of the [AWS::ApiGateway::RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html) resource\.

## Syntax<a name="aws-properties-apigateway-restapi-endpointconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-restapi-endpointconfiguration-syntax.json"></a>

```
{
  "[Types](#cfn-apigateway-restapi-endpointconfiguration-types)" : [ String, ... ],
  "[VpcEndpointIds](#cfn-apigateway-restapi-endpointconfiguration-vpcendpointids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-apigateway-restapi-endpointconfiguration-syntax.yaml"></a>

```
  [Types](#cfn-apigateway-restapi-endpointconfiguration-types): 
    - String
  [VpcEndpointIds](#cfn-apigateway-restapi-endpointconfiguration-vpcendpointids): 
    - String
```

## Properties<a name="aws-properties-apigateway-restapi-endpointconfiguration-properties"></a>

`Types`  <a name="cfn-apigateway-restapi-endpointconfiguration-types"></a>
A list of endpoint types of an API \(RestApi\) or its custom domain name \(DomainName\)\. For an edge\-optimized API and its custom domain name, the endpoint type is `"EDGE"`\. For a regional API and its custom domain name, the endpoint type is `REGIONAL`\. For a private API, the endpoint type is `PRIVATE`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcEndpointIds`  <a name="cfn-apigateway-restapi-endpointconfiguration-vpcendpointids"></a>
A list of VpcEndpointIds of an API \(RestApi\) against which to create Route53 ALIASes\. It is only supported for `PRIVATE` endpoint type\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-restapi-endpointconfiguration--seealso"></a>
+ [RestApi](https://docs.aws.amazon.com/apigateway/latest/api/API_RestApi.html) in the *Amazon API Gateway REST API Reference*

