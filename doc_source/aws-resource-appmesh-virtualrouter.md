# AWS::AppMesh::VirtualRouter<a name="aws-resource-appmesh-virtualrouter"></a>

Creates a virtual router within a service mesh\.

Specify a `listener` for any inbound traffic that your virtual router receives\. Create a virtual router for each protocol and port that you need to route\. Virtual routers handle traffic for one or more virtual services within your mesh\. After you create your virtual router, create and associate routes for your virtual router that direct incoming requests to different virtual nodes\.

For more information about virtual routers, see [Virtual routers](https://docs.aws.amazon.com/app-mesh/latest/userguide/virtual_routers.html)\.

## Syntax<a name="aws-resource-appmesh-virtualrouter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appmesh-virtualrouter-syntax.json"></a>

```
{
  "Type" : "AWS::AppMesh::VirtualRouter",
  "Properties" : {
      "[MeshName](#cfn-appmesh-virtualrouter-meshname)" : String,
      "[MeshOwner](#cfn-appmesh-virtualrouter-meshowner)" : String,
      "[Spec](#cfn-appmesh-virtualrouter-spec)" : VirtualRouterSpec,
      "[Tags](#cfn-appmesh-virtualrouter-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VirtualRouterName](#cfn-appmesh-virtualrouter-virtualroutername)" : String
    }
}
```

### YAML<a name="aws-resource-appmesh-virtualrouter-syntax.yaml"></a>

```
Type: AWS::AppMesh::VirtualRouter
Properties: 
  [MeshName](#cfn-appmesh-virtualrouter-meshname): String
  [MeshOwner](#cfn-appmesh-virtualrouter-meshowner): String
  [Spec](#cfn-appmesh-virtualrouter-spec): 
    VirtualRouterSpec
  [Tags](#cfn-appmesh-virtualrouter-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VirtualRouterName](#cfn-appmesh-virtualrouter-virtualroutername): String
```

## Properties<a name="aws-resource-appmesh-virtualrouter-properties"></a>

`MeshName`  <a name="cfn-appmesh-virtualrouter-meshname"></a>
The name of the service mesh to create the virtual router in\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MeshOwner`  <a name="cfn-appmesh-virtualrouter-meshowner"></a>
The AWS IAM account ID of the service mesh owner\. If the account ID is not your own, then the account that you specify must share the mesh with your account before you can create the resource in the service mesh\. For more information about mesh sharing, see [Working with shared meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Spec`  <a name="cfn-appmesh-virtualrouter-spec"></a>
The virtual router specification to apply\.  
*Required*: Yes  
*Type*: [VirtualRouterSpec](aws-properties-appmesh-virtualrouter-virtualrouterspec.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appmesh-virtualrouter-tags"></a>
Optional metadata that you can apply to the virtual router to assist with categorization and organization\. Each tag consists of a key and an optional value, both of which you define\. Tag keys can have a maximum character length of 128 characters, and tag values can have a maximum length of 256 characters\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualRouterName`  <a name="cfn-appmesh-virtualrouter-virtualroutername"></a>
The name to use for the virtual router\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-appmesh-virtualrouter-return-values"></a>

### Ref<a name="aws-resource-appmesh-virtualrouter-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN\. For example:

 `{ "Ref": "myVirtualRouter" }` 

When you pass the logical ID of an `AWS::AppMesh::VirtualRouter` resource to the intrinsic Ref function, the function returns the virtual router ARN, such as `arn:aws:appmesh:us-east-1:555555555555:virtualRouter/myVirtualRouter `\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-appmesh-virtualrouter-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-appmesh-virtualrouter-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The full Amazon Resource Name \(ARN\) for the virtual router\.

`MeshName`  <a name="MeshName-fn::getatt"></a>
The name of the service mesh that the virtual router resides in\.

`MeshOwner`  <a name="MeshOwner-fn::getatt"></a>
The AWS IAM account ID of the service mesh owner\. If the account ID is not your own, then it's the ID of the account that shared the mesh with your account\. For more information about mesh sharing, see [Working with Shared Meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.

`ResourceOwner`  <a name="ResourceOwner-fn::getatt"></a>
The AWS IAM account ID of the resource owner\. If the account ID is not your own, then it's the ID of the mesh owner or of another account that the mesh is shared with\. For more information about mesh sharing, see [Working with Shared Meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.

`Uid`  <a name="Uid-fn::getatt"></a>
The unique identifier for the virtual router\.

`VirtualRouterName`  <a name="VirtualRouterName-fn::getatt"></a>
The name of the virtual router\.

## Examples<a name="aws-resource-appmesh-virtualrouter--examples"></a>

### Create a Virtual Router<a name="aws-resource-appmesh-virtualrouter--examples--Create_a_Virtual_Router"></a>

This example creates a basic virtual router with an HTTP port mapping and two tags\.

#### JSON<a name="aws-resource-appmesh-virtualrouter--examples--Create_a_Virtual_Router--json"></a>

```
{
  "Description": "Basic Test Virtual Router",
  "Resources": {
    "BasicVirtualRouter": {
      "Type": "AWS::AppMesh::VirtualRouter",
      "Properties": {
        "VirtualRouterName": "TestVirtualRouter",
        "MeshName": null,
        "Spec": {
          "Listeners": [
            {
              "PortMapping": {
                "Port": 8080,
                "Protocol": "http"
              }
            }
          ]
        },
        "Tags": [
          {
            "Key": "Key1",
            "Value": "Value1"
          },
          {
            "Key": "Key2",
            "Value": "Value2"
          }
        ]
      }
    }
  },
  "Outputs": {
    "VirtualRouterName": {
      "Description": "Name of the VirtualRouter",
      "Value": {
        "Fn::GetAtt": [
          "BasicVirtualRouter",
          "VirtualRouterName"
        ]
      }
    },
    "MeshName": {
      "Description": "Name of the Mesh",
      "Value": {
        "Fn::GetAtt": [
          "BasicVirtualRouter",
          "MeshName"
        ]
      }
    },
    "Arn": {
      "Description": "Arn of the VirtualRouter created",
      "Value": {
        "Fn::GetAtt": [
          "BasicVirtualRouter",
          "Arn"
        ]
      }
    },
    "Uid": {
      "Description": "Uid of the VirtualRouter created",
      "Value": {
        "Fn::GetAtt": [
          "BasicVirtualRouter",
          "Uid"
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-appmesh-virtualrouter--examples--Create_a_Virtual_Router--yaml"></a>

```
Description: Basic Test Virtual Router
Resources:
  BasicVirtualRouter:
    Type: AWS::AppMesh::VirtualRouter
    Properties:
      VirtualRouterName: TestVirtualRouter
      MeshName: 
      Spec:
        Listeners:
        - PortMapping:
            Port: 8080
            Protocol: http
      Tags:
      - Key: Key1
        Value: Value1
      - Key: Key2
        Value: Value2
Outputs:
  VirtualRouterName:
    Description: Name of the VirtualRouter
    Value:
      Fn::GetAtt:
      - BasicVirtualRouter
      - VirtualRouterName
  MeshName:
    Description: Name of the Mesh
    Value:
      Fn::GetAtt:
      - BasicVirtualRouter
      - MeshName
  Arn:
    Description: Arn of the VirtualRouter created
    Value:
      Fn::GetAtt:
      - BasicVirtualRouter
      - Arn
  Uid:
    Description: Uid of the VirtualRouter created
    Value:
      Fn::GetAtt:
      - BasicVirtualRouter
      - Uid
```

## See also<a name="aws-resource-appmesh-virtualrouter--seealso"></a>
+  [Virtual Routers](https://docs.aws.amazon.com/app-mesh/latest/userguide/virtual_routers.html) in the * AWS App Mesh User Guide *\.
+  [CreateVirtualRouter](https://docs.aws.amazon.com/app-mesh/latest/APIReference/API_CreateVirtualRouter.html) in the * AWS App Mesh API Reference *\.

