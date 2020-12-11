# AWS::AppMesh::GatewayRoute<a name="aws-resource-appmesh-gatewayroute"></a>

Creates a gateway route\.

A gateway route is attached to a virtual gateway and routes traffic to an existing virtual service\. If a route matches a request, it can distribute traffic to a target virtual service\.

For more information about gateway routes, see [Gateway routes](https://docs.aws.amazon.com/app-mesh/latest/userguide/gateway-routes.html)\.

## Syntax<a name="aws-resource-appmesh-gatewayroute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appmesh-gatewayroute-syntax.json"></a>

```
{
  "Type" : "AWS::AppMesh::GatewayRoute",
  "Properties" : {
      "[GatewayRouteName](#cfn-appmesh-gatewayroute-gatewayroutename)" : String,
      "[MeshName](#cfn-appmesh-gatewayroute-meshname)" : String,
      "[MeshOwner](#cfn-appmesh-gatewayroute-meshowner)" : String,
      "[Spec](#cfn-appmesh-gatewayroute-spec)" : GatewayRouteSpec,
      "[Tags](#cfn-appmesh-gatewayroute-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VirtualGatewayName](#cfn-appmesh-gatewayroute-virtualgatewayname)" : String
    }
}
```

### YAML<a name="aws-resource-appmesh-gatewayroute-syntax.yaml"></a>

```
Type: AWS::AppMesh::GatewayRoute
Properties: 
  [GatewayRouteName](#cfn-appmesh-gatewayroute-gatewayroutename): String
  [MeshName](#cfn-appmesh-gatewayroute-meshname): String
  [MeshOwner](#cfn-appmesh-gatewayroute-meshowner): String
  [Spec](#cfn-appmesh-gatewayroute-spec): 
    GatewayRouteSpec
  [Tags](#cfn-appmesh-gatewayroute-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VirtualGatewayName](#cfn-appmesh-gatewayroute-virtualgatewayname): String
```

## Properties<a name="aws-resource-appmesh-gatewayroute-properties"></a>

`GatewayRouteName`  <a name="cfn-appmesh-gatewayroute-gatewayroutename"></a>
The name of the gateway route\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MeshName`  <a name="cfn-appmesh-gatewayroute-meshname"></a>
The name of the service mesh that the resource resides in\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MeshOwner`  <a name="cfn-appmesh-gatewayroute-meshowner"></a>
The AWS IAM account ID of the service mesh owner\. If the account ID is not your own, then it's the ID of the account that shared the mesh with your account\. For more information about mesh sharing, see [Working with shared meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Spec`  <a name="cfn-appmesh-gatewayroute-spec"></a>
The specifications of the gateway route\.  
*Required*: Yes  
*Type*: [GatewayRouteSpec](aws-properties-appmesh-gatewayroute-gatewayroutespec.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appmesh-gatewayroute-tags"></a>
Optional metadata that you can apply to the gateway route to assist with categorization and organization\. Each tag consists of a key and an optional value, both of which you define\. Tag keys can have a maximum character length of 128 characters, and tag values can have a maximum length of 256 characters\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualGatewayName`  <a name="cfn-appmesh-gatewayroute-virtualgatewayname"></a>
The virtual gateway that the gateway route is associated with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-appmesh-gatewayroute-return-values"></a>

### Ref<a name="aws-resource-appmesh-gatewayroute-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN\. For example:

 `{ "Ref": "myGatewayRoute" }` 

When you pass the logical ID of an `AWS::AppMesh::GatewayRoute` resource to the intrinsic Ref function, the function returns the gateway route ARN, such as `arn:aws:appmesh:us-east-1:555555555555:gatewayRoute/myGatewayRoute `\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-appmesh-gatewayroute-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-appmesh-gatewayroute-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The full Amazon Resource Name \(ARN\) for the gateway route\.

`GatewayRouteName`  <a name="GatewayRouteName-fn::getatt"></a>
The name of the gateway route\.

`MeshName`  <a name="MeshName-fn::getatt"></a>
The name of the service mesh that the gateway route resides in\.

`MeshOwner`  <a name="MeshOwner-fn::getatt"></a>
The AWS IAM account ID of the service mesh owner\. If the account ID is not your own, then it's the ID of the account that shared the mesh with your account\. For more information about mesh sharing, see [Working with Shared Meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.

`ResourceOwner`  <a name="ResourceOwner-fn::getatt"></a>
The AWS IAM account ID of the resource owner\. If the account ID is not your own, then it's the ID of the mesh owner or of another account that the mesh is shared with\. For more information about mesh sharing, see [Working with Shared Meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.

`Uid`  <a name="Uid-fn::getatt"></a>
The unique identifier for the gateway route\.

`VirtualGatewayName`  <a name="VirtualGatewayName-fn::getatt"></a>
The name of the virtual gateway that the gateway route is associated with\.

## See also<a name="aws-resource-appmesh-gatewayroute--seealso"></a>
+  [Gateway routes](https://docs.aws.amazon.com/app-mesh/latest/userguide/gateway-routes.html) in the * AWS App Mesh User Guide *\.
+  [CreateGatewayRoute](https://docs.aws.amazon.com/app-mesh/latest/APIReference/API_CreateGatewayRoute.html) in the * AWS App Mesh API Reference *\.

