# AWS::AppMesh::Route GrpcRouteMatch<a name="aws-properties-appmesh-route-grpcroutematch"></a>

An object that represents the criteria for determining a request match\.

## Syntax<a name="aws-properties-appmesh-route-grpcroutematch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-grpcroutematch-syntax.json"></a>

```
{
  "[Metadata](#cfn-appmesh-route-grpcroutematch-metadata)" : [ GrpcRouteMetadata, ... ],
  "[MethodName](#cfn-appmesh-route-grpcroutematch-methodname)" : String,
  "[ServiceName](#cfn-appmesh-route-grpcroutematch-servicename)" : String
}
```

### YAML<a name="aws-properties-appmesh-route-grpcroutematch-syntax.yaml"></a>

```
  [Metadata](#cfn-appmesh-route-grpcroutematch-metadata): 
    - GrpcRouteMetadata
  [MethodName](#cfn-appmesh-route-grpcroutematch-methodname): String
  [ServiceName](#cfn-appmesh-route-grpcroutematch-servicename): String
```

## Properties<a name="aws-properties-appmesh-route-grpcroutematch-properties"></a>

`Metadata`  <a name="cfn-appmesh-route-grpcroutematch-metadata"></a>
An object that represents the data to match from the request\.  
*Required*: No  
*Type*: List of [GrpcRouteMetadata](aws-properties-appmesh-route-grpcroutemetadata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MethodName`  <a name="cfn-appmesh-route-grpcroutematch-methodname"></a>
The method name to match from the request\. If you specify a name, you must also specify a `serviceName`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceName`  <a name="cfn-appmesh-route-grpcroutematch-servicename"></a>
The fully qualified domain name for the service to match from the request\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)