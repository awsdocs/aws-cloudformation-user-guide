# AWS::AppMesh::GatewayRoute QueryParameter<a name="aws-properties-appmesh-gatewayroute-queryparameter"></a>

An object that represents the query parameter in the request\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-queryparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-queryparameter-syntax.json"></a>

```
{
  "[Match](#cfn-appmesh-gatewayroute-queryparameter-match)" : HttpQueryParameterMatch,
  "[Name](#cfn-appmesh-gatewayroute-queryparameter-name)" : String
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-queryparameter-syntax.yaml"></a>

```
  [Match](#cfn-appmesh-gatewayroute-queryparameter-match): 
    HttpQueryParameterMatch
  [Name](#cfn-appmesh-gatewayroute-queryparameter-name): String
```

## Properties<a name="aws-properties-appmesh-gatewayroute-queryparameter-properties"></a>

`Match`  <a name="cfn-appmesh-gatewayroute-queryparameter-match"></a>
The query parameter to match on\.  
*Required*: No  
*Type*: [HttpQueryParameterMatch](aws-properties-appmesh-gatewayroute-httpqueryparametermatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appmesh-gatewayroute-queryparameter-name"></a>
A name for the query parameter that will be matched on\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)