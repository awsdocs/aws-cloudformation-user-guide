# AWS::AppMesh::Route<a name="aws-resource-appmesh-route"></a>

Creates a route that is associated with a virtual router\.

 You can route several different protocols and define a retry policy for a route\. Traffic can be routed to one or more virtual nodes\.

For more information about routes, see [Routes](https://docs.aws.amazon.com/app-mesh/latest/userguide/routes.html)\.

## Syntax<a name="aws-resource-appmesh-route-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appmesh-route-syntax.json"></a>

```
{
  "Type" : "AWS::AppMesh::Route",
  "Properties" : {
      "[MeshName](#cfn-appmesh-route-meshname)" : String,
      "[MeshOwner](#cfn-appmesh-route-meshowner)" : String,
      "[RouteName](#cfn-appmesh-route-routename)" : String,
      "[Spec](#cfn-appmesh-route-spec)" : RouteSpec,
      "[Tags](#cfn-appmesh-route-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VirtualRouterName](#cfn-appmesh-route-virtualroutername)" : String
    }
}
```

### YAML<a name="aws-resource-appmesh-route-syntax.yaml"></a>

```
Type: AWS::AppMesh::Route
Properties: 
  [MeshName](#cfn-appmesh-route-meshname): String
  [MeshOwner](#cfn-appmesh-route-meshowner): String
  [RouteName](#cfn-appmesh-route-routename): String
  [Spec](#cfn-appmesh-route-spec): 
    RouteSpec
  [Tags](#cfn-appmesh-route-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VirtualRouterName](#cfn-appmesh-route-virtualroutername): String
```

## Properties<a name="aws-resource-appmesh-route-properties"></a>

`MeshName`  <a name="cfn-appmesh-route-meshname"></a>
The name of the service mesh to create the route in\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MeshOwner`  <a name="cfn-appmesh-route-meshowner"></a>
The AWS IAM account ID of the service mesh owner\. If the account ID is not your own, then the account that you specify must share the mesh with your account before you can create the resource in the service mesh\. For more information about mesh sharing, see [Working with shared meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RouteName`  <a name="cfn-appmesh-route-routename"></a>
The name to use for the route\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Spec`  <a name="cfn-appmesh-route-spec"></a>
The route specification to apply\.  
*Required*: Yes  
*Type*: [RouteSpec](aws-properties-appmesh-route-routespec.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appmesh-route-tags"></a>
Optional metadata that you can apply to the route to assist with categorization and organization\. Each tag consists of a key and an optional value, both of which you define\. Tag keys can have a maximum character length of 128 characters, and tag values can have a maximum length of 256 characters\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualRouterName`  <a name="cfn-appmesh-route-virtualroutername"></a>
The name of the virtual router in which to create the route\. If the virtual router is in a shared mesh, then you must be the owner of the virtual router resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-appmesh-route-return-values"></a>

### Ref<a name="aws-resource-appmesh-route-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN\. For example:

 `{ "Ref": "myRoute" }` 

When you pass the logical ID of an `AWS::AppMesh::Route` resource to the intrinsic Ref function, the function returns the route ARN, such as `arn:aws:appmesh:us-east-1:555555555555:route/myRoute `\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-appmesh-route-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-appmesh-route-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The full Amazon Resource Name \(ARN\) for the route\.

`MeshName`  <a name="MeshName-fn::getatt"></a>
The name of the service mesh that the route resides in\.

`MeshOwner`  <a name="MeshOwner-fn::getatt"></a>
The AWS IAM account ID of the service mesh owner\. If the account ID is not your own, then it's the ID of the account that shared the mesh with your account\. For more information about mesh sharing, see [Working with Shared Meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.

`ResourceOwner`  <a name="ResourceOwner-fn::getatt"></a>
The AWS IAM account ID of the resource owner\. If the account ID is not your own, then it's the ID of the mesh owner or of another account that the mesh is shared with\. For more information about mesh sharing, see [Working with Shared Meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.

`RouteName`  <a name="RouteName-fn::getatt"></a>
The name of the route\.

`Uid`  <a name="Uid-fn::getatt"></a>
The unique identifier for the route\.

`VirtualRouterName`  <a name="VirtualRouterName-fn::getatt"></a>
The name of the virtual router that the route is associated with\.

## Examples<a name="aws-resource-appmesh-route--examples"></a>

### Create a Route<a name="aws-resource-appmesh-route--examples--Create_a_Route"></a>

This example creates a route with two weighted targets\.

#### JSON<a name="aws-resource-appmesh-route--examples--Create_a_Route--json"></a>

```
{
   "Description": "Basic Test Route",
   "Resources": {
      "BasicRoute": {
         "Type": "AWS::AppMesh::Route",
         "Properties": {
            "RouteName": "TestRoute",
            "MeshName": null,
            "VirtualRouterName": null,
            "Spec": {
               "HttpRoute": {
                  "Match": {
                     "Prefix": "routePrefix"
                  },
                  "Action": {
                     "WeightedTargets": [
                        {
                           "VirtualNode": null,
                           "Weight": 10
                        },
                        {
                           "VirtualNode": null,
                           "Weight": 20
                        }
                     ]
                  }
               }
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
      "RouteName": {
         "Description": "Name of the Route",
         "Value": {
            "Fn::GetAtt": [
               "BasicRoute",
               "RouteName"
            ]
         }
      },
      "MeshName": {
         "Description": "Name of the Mesh",
         "Value": {
            "Fn::GetAtt": [
               "BasicRoute",
               "MeshName"
            ]
         }
      },
      "VirtualRouterName": {
         "Description": "Name of the VirtualRouter",
         "Value": {
            "Fn::GetAtt": [
               "BasicRoute",
               "VirtualRouterName"
            ]
         }
      },
      "Arn": {
         "Description": "Arn of the Route created",
         "Value": {
            "Fn::GetAtt": [
               "BasicRoute",
               "Arn"
            ]
         }
      },
      "Uid": {
         "Description": "Uid of the Route created",
         "Value": {
            "Fn::GetAtt": [
               "BasicRoute",
               "Uid"
            ]
         }
      }
   }
}
```

#### YAML<a name="aws-resource-appmesh-route--examples--Create_a_Route--yaml"></a>

```
Description: "Basic Test Route"
Resources:
  BasicRoute:
    Type: "AWS::AppMesh::Route"
    Properties:
      RouteName: "TestRoute"
      MeshName: !ImportValue TestMeshName
      VirtualRouterName: !ImportValue TestVirtualRouterName1
      Spec:
        HttpRoute:
          Match:
            Prefix: "routePrefix"
          Action:
            WeightedTargets:
            - VirtualNode: !ImportValue TestVirtualNodeName1
              Weight: 10
            - VirtualNode: !ImportValue TestVirtualNodeName2
              Weight: 20
      Tags:
      - Key: "Key1"
        Value: "Value1"
      - Key: "Key2"
        Value: "Value2"

Outputs:
  RouteName:
    Description: Name of the Route
    Value:
      Fn::GetAtt:
      - BasicRoute
      - RouteName
  MeshName:
    Description: Name of the Mesh
    Value:
      Fn::GetAtt:
      - BasicRoute
      - MeshName
  VirtualRouterName:
    Description: Name of the VirtualRouter
    Value:
      Fn::GetAtt:
      - BasicRoute
      - VirtualRouterName
  Arn:
    Description: Arn of the Route created
    Value:
      Fn::GetAtt:
      - BasicRoute
      - Arn
  Uid:
    Description: Uid of the Route created
    Value:
      Fn::GetAtt:
      - BasicRoute
      - Uid
```

## See also<a name="aws-resource-appmesh-route--seealso"></a>
+  [Routes](https://docs.aws.amazon.com/app-mesh/latest/userguide/routes.html) in the * AWS App Mesh User Guide *\.
+  [CreateRoute](https://docs.aws.amazon.com/app-mesh/latest/APIReference/API_CreateRoute.html) in the * AWS App Mesh API Reference *\.

