# AWS::AppMesh::VirtualService<a name="aws-resource-appmesh-virtualservice"></a>

Creates a virtual service within a service mesh\.

A virtual service is an abstraction of a real service that is provided by a virtual node directly or indirectly by means of a virtual router\. Dependent services call your virtual service by its `virtualServiceName`, and those requests are routed to the virtual node or virtual router that is specified as the provider for the virtual service\.

For more information about virtual services, see [Virtual services](https://docs.aws.amazon.com/app-mesh/latest/userguide/virtual_services.html)\.

## Syntax<a name="aws-resource-appmesh-virtualservice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appmesh-virtualservice-syntax.json"></a>

```
{
  "Type" : "AWS::AppMesh::VirtualService",
  "Properties" : {
      "[MeshName](#cfn-appmesh-virtualservice-meshname)" : String,
      "[MeshOwner](#cfn-appmesh-virtualservice-meshowner)" : String,
      "[Spec](#cfn-appmesh-virtualservice-spec)" : VirtualServiceSpec,
      "[Tags](#cfn-appmesh-virtualservice-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VirtualServiceName](#cfn-appmesh-virtualservice-virtualservicename)" : String
    }
}
```

### YAML<a name="aws-resource-appmesh-virtualservice-syntax.yaml"></a>

```
Type: AWS::AppMesh::VirtualService
Properties: 
  [MeshName](#cfn-appmesh-virtualservice-meshname): String
  [MeshOwner](#cfn-appmesh-virtualservice-meshowner): String
  [Spec](#cfn-appmesh-virtualservice-spec): 
    VirtualServiceSpec
  [Tags](#cfn-appmesh-virtualservice-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VirtualServiceName](#cfn-appmesh-virtualservice-virtualservicename): String
```

## Properties<a name="aws-resource-appmesh-virtualservice-properties"></a>

`MeshName`  <a name="cfn-appmesh-virtualservice-meshname"></a>
The name of the service mesh to create the virtual service in\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MeshOwner`  <a name="cfn-appmesh-virtualservice-meshowner"></a>
The AWS IAM account ID of the service mesh owner\. If the account ID is not your own, then the account that you specify must share the mesh with your account before you can create the resource in the service mesh\. For more information about mesh sharing, see [Working with shared meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Spec`  <a name="cfn-appmesh-virtualservice-spec"></a>
The virtual service specification to apply\.  
*Required*: Yes  
*Type*: [VirtualServiceSpec](aws-properties-appmesh-virtualservice-virtualservicespec.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appmesh-virtualservice-tags"></a>
Optional metadata that you can apply to the virtual service to assist with categorization and organization\. Each tag consists of a key and an optional value, both of which you define\. Tag keys can have a maximum character length of 128 characters, and tag values can have a maximum length of 256 characters\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualServiceName`  <a name="cfn-appmesh-virtualservice-virtualservicename"></a>
The name to use for the virtual service\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-appmesh-virtualservice-return-values"></a>

### Ref<a name="aws-resource-appmesh-virtualservice-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN\. For example:

 `{ "Ref": "myVirtualService" }` 

When you pass the logical ID of an `AWS::AppMesh::VirtualService` resource to the intrinsic Ref function, the function returns the virtual service ARN, such as `arn:aws:appmesh:us-east-1:555555555555:virtualService/myVirtualService `\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-appmesh-virtualservice-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-appmesh-virtualservice-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The full Amazon Resource Name \(ARN\) for the virtual service\.

`MeshName`  <a name="MeshName-fn::getatt"></a>
The name of the service mesh that the virtual service resides in\.

`MeshOwner`  <a name="MeshOwner-fn::getatt"></a>
The AWS IAM account ID of the service mesh owner\. If the account ID is not your own, then it's the ID of the account that shared the mesh with your account\. For more information about mesh sharing, see [Working with Shared Meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.

`ResourceOwner`  <a name="ResourceOwner-fn::getatt"></a>
The AWS IAM account ID of the resource owner\. If the account ID is not your own, then it's the ID of the mesh owner or of another account that the mesh is shared with\. For more information about mesh sharing, see [Working with Shared Meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.

`Uid`  <a name="Uid-fn::getatt"></a>
The unique identifier for the virtual service\.

`VirtualServiceName`  <a name="VirtualServiceName-fn::getatt"></a>
The name of the virtual service\.

## See also<a name="aws-resource-appmesh-virtualservice--seealso"></a>
+  [Virtual Services](https://docs.aws.amazon.com/app-mesh/latest/userguide/virtual_services.html) in the * AWS App Mesh User Guide *\.
+  [CreateVirtualService](https://docs.aws.amazon.com/app-mesh/latest/APIReference/API_CreateVirtualService.html) in the * AWS App Mesh API Reference *\.

