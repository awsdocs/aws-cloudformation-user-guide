# AWS::AppMesh::VirtualGateway<a name="aws-resource-appmesh-virtualgateway"></a>

Creates a virtual gateway\.

A virtual gateway allows resources outside your mesh to communicate to resources that are inside your mesh\. The virtual gateway represents an Envoy proxy running in an Amazon ECS task, in a Kubernetes service, or on an Amazon EC2 instance\. Unlike a virtual node, which represents an Envoy running with an application, a virtual gateway represents Envoy deployed by itself\.

For more information about virtual gateways, see [Virtual gateways](https://docs.aws.amazon.com/app-mesh/latest/userguide/virtual_gateways.html)\. 

## Syntax<a name="aws-resource-appmesh-virtualgateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appmesh-virtualgateway-syntax.json"></a>

```
{
  "Type" : "AWS::AppMesh::VirtualGateway",
  "Properties" : {
      "[MeshName](#cfn-appmesh-virtualgateway-meshname)" : String,
      "[MeshOwner](#cfn-appmesh-virtualgateway-meshowner)" : String,
      "[Spec](#cfn-appmesh-virtualgateway-spec)" : VirtualGatewaySpec,
      "[Tags](#cfn-appmesh-virtualgateway-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VirtualGatewayName](#cfn-appmesh-virtualgateway-virtualgatewayname)" : String
    }
}
```

### YAML<a name="aws-resource-appmesh-virtualgateway-syntax.yaml"></a>

```
Type: AWS::AppMesh::VirtualGateway
Properties: 
  [MeshName](#cfn-appmesh-virtualgateway-meshname): String
  [MeshOwner](#cfn-appmesh-virtualgateway-meshowner): String
  [Spec](#cfn-appmesh-virtualgateway-spec): 
    VirtualGatewaySpec
  [Tags](#cfn-appmesh-virtualgateway-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VirtualGatewayName](#cfn-appmesh-virtualgateway-virtualgatewayname): String
```

## Properties<a name="aws-resource-appmesh-virtualgateway-properties"></a>

`MeshName`  <a name="cfn-appmesh-virtualgateway-meshname"></a>
The name of the service mesh that the virtual gateway resides in\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MeshOwner`  <a name="cfn-appmesh-virtualgateway-meshowner"></a>
The AWS IAM account ID of the service mesh owner\. If the account ID is not your own, then it's the ID of the account that shared the mesh with your account\. For more information about mesh sharing, see [Working with shared meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Spec`  <a name="cfn-appmesh-virtualgateway-spec"></a>
The specifications of the virtual gateway\.  
*Required*: Yes  
*Type*: [VirtualGatewaySpec](aws-properties-appmesh-virtualgateway-virtualgatewayspec.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appmesh-virtualgateway-tags"></a>
Optional metadata that you can apply to the virtual gateway to assist with categorization and organization\. Each tag consists of a key and an optional value, both of which you define\. Tag keys can have a maximum character length of 128 characters, and tag values can have a maximum length of 256 characters\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualGatewayName`  <a name="cfn-appmesh-virtualgateway-virtualgatewayname"></a>
The name of the virtual gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-appmesh-virtualgateway-return-values"></a>

### Ref<a name="aws-resource-appmesh-virtualgateway-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN\. For example:

 `{ "Ref": "myVirtualGateway" }` 

When you pass the logical ID of an `AWS::AppMesh::VirtualGateway` resource to the intrinsic Ref function, the function returns the gateway route ARN, such as `arn:aws:appmesh:us-east-1:555555555555:virtualGateway/myVirtualGateway `\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-appmesh-virtualgateway-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-appmesh-virtualgateway-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The full Amazon Resource Name \(ARN\) for the virtual gateway\.

`MeshName`  <a name="MeshName-fn::getatt"></a>
The name of the service mesh that the virtual gateway resides in\.

`MeshOwner`  <a name="MeshOwner-fn::getatt"></a>
The AWS IAM account ID of the service mesh owner\. If the account ID is not your own, then it's the ID of the account that shared the mesh with your account\. For more information about mesh sharing, see [Working with Shared Meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.

`ResourceOwner`  <a name="ResourceOwner-fn::getatt"></a>
The AWS IAM account ID of the resource owner\. If the account ID is not your own, then it's the ID of the mesh owner or of another account that the mesh is shared with\. For more information about mesh sharing, see [Working with Shared Meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.

`Uid`  <a name="Uid-fn::getatt"></a>
The unique identifier for the virtual gateway\.

`VirtualGatewayName`  <a name="VirtualGatewayName-fn::getatt"></a>
The name of the virtual gateway\.

## See also<a name="aws-resource-appmesh-virtualgateway--seealso"></a>
+  [Virtual gateways](https://docs.aws.amazon.com/app-mesh/latest/userguide/virtual_gateways.html) in the * AWS App Mesh User Guide *\.
+  [CreateVirtualGateway](https://docs.aws.amazon.com/app-mesh/latest/APIReference/API_CreateVirtualGateway.html) in the * AWS App Mesh API Reference *\.

