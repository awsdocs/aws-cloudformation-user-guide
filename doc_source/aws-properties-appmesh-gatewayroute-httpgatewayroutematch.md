# AWS::AppMesh::GatewayRoute HttpGatewayRouteMatch<a name="aws-properties-appmesh-gatewayroute-httpgatewayroutematch"></a>

An object that represents the criteria for determining a request match\.

## Syntax<a name="aws-properties-appmesh-gatewayroute-httpgatewayroutematch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-gatewayroute-httpgatewayroutematch-syntax.json"></a>

```
{
  "[Prefix](#cfn-appmesh-gatewayroute-httpgatewayroutematch-prefix)" : String
}
```

### YAML<a name="aws-properties-appmesh-gatewayroute-httpgatewayroutematch-syntax.yaml"></a>

```
  [Prefix](#cfn-appmesh-gatewayroute-httpgatewayroutematch-prefix): String
```

## Properties<a name="aws-properties-appmesh-gatewayroute-httpgatewayroutematch-properties"></a>

`Prefix`  <a name="cfn-appmesh-gatewayroute-httpgatewayroutematch-prefix"></a>
Specifies the path to match requests with\. This parameter must always start with `/`, which by itself matches all requests to the virtual service name\. You can also match for path\-based routing of requests\. For example, if your virtual service name is `my-service.local` and you want the route to match requests to `my-service.local/metrics`, your prefix should be `/metrics`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)