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
A list of endpoint types of an API or its custom domain name\. Valid values include:  
+ `EDGE`: For an edge\-optimized API and its custom domain name\.
+ `REGIONAL`: For a regional API and its custom domain name\.
+ `PRIVATE`: For a private API\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcEndpointIds`  <a name="cfn-apigateway-restapi-endpointconfiguration-vpcendpointids"></a>
A list of VPC endpoint IDs of an API \([AWS::ApiGateway::RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html)\) against which to create Route53 ALIASes\. It is only supported for `PRIVATE` endpoint type\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-restapi-endpointconfiguration--seealso"></a>
+ [RestApi](https://docs.aws.amazon.com/apigateway/api-reference/resource/rest-api/) in the *Amazon API Gateway REST API Reference*

