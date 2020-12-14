# AWS::AppMesh::Mesh<a name="aws-resource-appmesh-mesh"></a>

Creates a service mesh\.

 A service mesh is a logical boundary for network traffic between services that are represented by resources within the mesh\. After you create your service mesh, you can create virtual services, virtual nodes, virtual routers, and routes to distribute traffic between the applications in your mesh\.

For more information about service meshes, see [Service meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/meshes.html)\.

## Syntax<a name="aws-resource-appmesh-mesh-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appmesh-mesh-syntax.json"></a>

```
{
  "Type" : "AWS::AppMesh::Mesh",
  "Properties" : {
      "[MeshName](#cfn-appmesh-mesh-meshname)" : String,
      "[Spec](#cfn-appmesh-mesh-spec)" : MeshSpec,
      "[Tags](#cfn-appmesh-mesh-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-appmesh-mesh-syntax.yaml"></a>

```
Type: AWS::AppMesh::Mesh
Properties: 
  [MeshName](#cfn-appmesh-mesh-meshname): String
  [Spec](#cfn-appmesh-mesh-spec): 
    MeshSpec
  [Tags](#cfn-appmesh-mesh-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-appmesh-mesh-properties"></a>

`MeshName`  <a name="cfn-appmesh-mesh-meshname"></a>
The name to use for the service mesh\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Spec`  <a name="cfn-appmesh-mesh-spec"></a>
The service mesh specification to apply\.  
*Required*: No  
*Type*: [MeshSpec](aws-properties-appmesh-mesh-meshspec.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appmesh-mesh-tags"></a>
Optional metadata that you can apply to the service mesh to assist with categorization and organization\. Each tag consists of a key and an optional value, both of which you define\. Tag keys can have a maximum character length of 128 characters, and tag values can have a maximum length of 256 characters\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appmesh-mesh-return-values"></a>

### Ref<a name="aws-resource-appmesh-mesh-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN\. For example:

 `{ "Ref": "myMesh" }` 

When you pass the logical ID of an `AWS::AppMesh::Mesh` resource to the intrinsic Ref function, the function returns the mesh ARN, such as `arn:aws:appmesh:us-east-1:555555555555:mesh/myMesh `\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-appmesh-mesh-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-appmesh-mesh-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The full Amazon Resource Name \(ARN\) for the mesh\.

`MeshName`  <a name="MeshName-fn::getatt"></a>
The name of the service mesh\.

`MeshOwner`  <a name="MeshOwner-fn::getatt"></a>
The AWS IAM account ID of the service mesh owner\. If the account ID is not your own, then it's the ID of the account that shared the mesh with your account\. For more information about mesh sharing, see [Working with Shared Meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.

`ResourceOwner`  <a name="ResourceOwner-fn::getatt"></a>
The AWS IAM account ID of the resource owner\. If the account ID is not your own, then it's the ID of the mesh owner or of another account that the mesh is shared with\. For more information about mesh sharing, see [Working with Shared Meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/sharing.html)\.

`Uid`  <a name="Uid-fn::getatt"></a>
The unique identifier for the mesh\.

## Examples<a name="aws-resource-appmesh-mesh--examples"></a>

### Create a Service Mesh<a name="aws-resource-appmesh-mesh--examples--Create_a_Service_Mesh"></a>

This example creates a service mesh that allows all egress traffic\.

#### JSON<a name="aws-resource-appmesh-mesh--examples--Create_a_Service_Mesh--json"></a>

```
{
   "Description": "Basic Test Mesh",
   "Resources": {
      "BasicMesh": {
         "Type": "AWS::AppMesh::Mesh",
         "Properties": {
            "MeshName": "BasicMesh1",
            "Spec": {
               "EgressFilter": {
                  "Type": "ALLOW_ALL"
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
      "MeshName": {
         "Description": "Name of the Mesh",
         "Value": {
            "Fn::GetAtt": [
               "BasicMesh",
               "MeshName"
            ]
         }
      },
      "Arn": {
         "Description": "Arn of the Mesh created",
         "Value": {
            "Fn::GetAtt": [
               "BasicMesh",
               "Arn"
            ]
         }
      },
      "Uid": {
         "Description": "Uid of the Mesh created",
         "Value": {
            "Fn::GetAtt": [
               "BasicMesh",
               "Uid"
            ]
         }
      }
   }
}
```

#### YAML<a name="aws-resource-appmesh-mesh--examples--Create_a_Service_Mesh--yaml"></a>

```
Description: "Basic Test Mesh"
Resources:
  BasicMesh:
    Type: "AWS::AppMesh::Mesh"
    Properties:
      MeshName: "BasicMesh1"
      Spec:
        EgressFilter:
          Type: "ALLOW_ALL"
      Tags:
      - Key: "Key1"
        Value: "Value1"
      - Key: "Key2"
        Value: "Value2"
Outputs:
  MeshName:
    Description: Name of the Mesh
    Value:
      Fn::GetAtt:
      - BasicMesh
      - MeshName
  Arn:
    Description: Arn of the Mesh created
    Value:
      Fn::GetAtt:
      - BasicMesh
      - Arn
  Uid:
    Description: Uid of the Mesh created
    Value:
      Fn::GetAtt:
      - BasicMesh
      - Uid
```

## See also<a name="aws-resource-appmesh-mesh--seealso"></a>
+  [Service Meshes](https://docs.aws.amazon.com/app-mesh/latest/userguide/meshes.html) in the * AWS App Mesh User Guide *\.
+  [CreateMesh](https://docs.aws.amazon.com/app-mesh/latest/APIReference/API_CreateMesh.html) in the * AWS App Mesh API Reference *\.

