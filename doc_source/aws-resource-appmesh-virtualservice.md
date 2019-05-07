# AWS::AppMesh::VirtualService<a name="aws-resource-appmesh-virtualservice"></a>

Creates a virtual service within a service mesh\.

A virtual service is an abstraction of a real service that is provided by a virtual node directly or indirectly by means of a virtual router\. Dependent services call your virtual service by its `virtualServiceName`, and those requests are routed to the virtual node or virtual router that is specified as the provider for the virtual service\.

## Syntax<a name="aws-resource-appmesh-virtualservice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appmesh-virtualservice-syntax.json"></a>

```
{
  "Type" : "AWS::AppMesh::VirtualService",
  "Properties" : {
      "[MeshName](#cfn-appmesh-virtualservice-meshname)" : String,
      "[Spec](#cfn-appmesh-virtualservice-spec)" : [VirtualServiceSpec](aws-properties-appmesh-virtualservice-virtualservicespec.md),
      "[Tags](#cfn-appmesh-virtualservice-tags)" : [ [TagRef](aws-properties-appmesh-virtualservice-tagref.md), ... ],
      "[VirtualServiceName](#cfn-appmesh-virtualservice-virtualservicename)" : String
    }
}
```

### YAML<a name="aws-resource-appmesh-virtualservice-syntax.yaml"></a>

```
Type: AWS::AppMesh::VirtualService
Properties : 
﻿  [MeshName](#cfn-appmesh-virtualservice-meshname) : String
﻿  [Spec](#cfn-appmesh-virtualservice-spec) : 
    [VirtualServiceSpec](aws-properties-appmesh-virtualservice-virtualservicespec.md)
﻿  [Tags](#cfn-appmesh-virtualservice-tags) : 
    - [TagRef](aws-properties-appmesh-virtualservice-tagref.md)
﻿  [VirtualServiceName](#cfn-appmesh-virtualservice-virtualservicename) : String
```

## Properties<a name="aws-resource-appmesh-virtualservice-properties"></a>

`MeshName`  <a name="cfn-appmesh-virtualservice-meshname"></a>
The name of the service mesh to create the virtual service in\.  
*Required*: Yes  
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
*Type*: List of [TagRef](aws-properties-appmesh-virtualservice-tagref.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualServiceName`  <a name="cfn-appmesh-virtualservice-virtualservicename"></a>
The name to use for the virtual service\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-appmesh-virtualservice-return-values"></a>

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

`Uid`  <a name="Uid-fn::getatt"></a>
The unique identifier for the virtual service\.

`VirtualServiceName`  <a name="VirtualServiceName-fn::getatt"></a>
The name of the virtual service\.

## Examples<a name="aws-resource-appmesh-virtualservice--examples"></a>

### Create a Virtual Service<a name="aws-resource-appmesh-virtualservice--examples--Create_a_Virtual_Service"></a>

This example creates a virtual service that is provided by a virtual node\.

#### JSON<a name="aws-resource-appmesh-virtualservice--examples--Create_a_Virtual_Service--json"></a>

```
{
   "Description": "Basic Test VirtualService",
   "Resources": {
      "BasicVirtualService1": {
         "Type": "AWS::AppMesh::VirtualService",
         "Properties": {
            "VirtualServiceName": "TestVirtualService1.internal",
            "MeshName": null,
            "Spec": {
               "Provider": {
                  "VirtualNode": {
                     "VirtualNodeName": null
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
      "VirtualServiceName1": {
         "Description": "Name of the VirtualService",
         "Value": {
            "Fn::GetAtt": [
               "BasicVirtualService1",
               "VirtualServiceName"
            ]
         }
      },
      "MeshName": {
         "Description": "Name of the Mesh",
         "Value": {
            "Fn::GetAtt": [
               "BasicVirtualService1",
               "MeshName"
            ]
         }
      },
      "Arn": {
         "Description": "Arn of the VirtualService created",
         "Value": {
            "Fn::GetAtt": [
               "BasicVirtualService1",
               "Arn"
            ]
         }
      },
      "Uid": {
         "Description": "Uid of the VirtualService created",
         "Value": {
            "Fn::GetAtt": [
               "BasicVirtualService1",
               "Uid"
            ]
         }
      }
   }
}
```

#### YAML<a name="aws-resource-appmesh-virtualservice--examples--Create_a_Virtual_Service--yaml"></a>

```
Description: "Basic Test VirtualService"
Resources:
  BasicVirtualService1:
    Type: "AWS::AppMesh::VirtualService"
    Properties:
      VirtualServiceName: "TestVirtualService1.internal"
      MeshName: !ImportValue TestMeshName
      Spec:
        Provider:
          VirtualNode:
            VirtualNodeName: !ImportValue TestVirtualNodeName1
      Tags:
      - Key: "Key1"
        Value: "Value1"
      - Key: "Key2"
        Value: "Value2"

Outputs:
  VirtualServiceName1:
    Description: Name of the VirtualService
    Value:
      Fn::GetAtt:
        - BasicVirtualService1
        - VirtualServiceName
  MeshName:
    Description: Name of the Mesh
    Value:
      Fn::GetAtt:
        - BasicVirtualService1
        - MeshName
  Arn:
    Description: Arn of the VirtualService created
    Value:
      Fn::GetAtt:
        - BasicVirtualService1
        - Arn
  Uid:
    Description: Uid of the VirtualService created
    Value:
      Fn::GetAtt:
        - BasicVirtualService1
        - Uid
```

## See Also<a name="aws-resource-appmesh-virtualservice--seealso"></a>
+  [Virtual Services](https://docs.aws.amazon.com/app-mesh/latest/userguide/virtual_services.html) in the * AWS App Mesh User Guide *\.
+  [CreateVirtualService](https://docs.aws.amazon.com/app-mesh/latest/APIReference/API_CreateVirtualService.html) in the * AWS App Mesh API Reference *\.