# AWS::AppMesh::VirtualService VirtualServiceProvider<a name="aws-properties-appmesh-virtualservice-virtualserviceprovider"></a>

An object that represents the provider for a virtual service\.

## Syntax<a name="aws-properties-appmesh-virtualservice-virtualserviceprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualservice-virtualserviceprovider-syntax.json"></a>

```
{
  "[VirtualNode](#cfn-appmesh-virtualservice-virtualserviceprovider-virtualnode)" : VirtualNodeServiceProvider,
  "[VirtualRouter](#cfn-appmesh-virtualservice-virtualserviceprovider-virtualrouter)" : VirtualRouterServiceProvider
}
```

### YAML<a name="aws-properties-appmesh-virtualservice-virtualserviceprovider-syntax.yaml"></a>

```
  [VirtualNode](#cfn-appmesh-virtualservice-virtualserviceprovider-virtualnode): 
    VirtualNodeServiceProvider
  [VirtualRouter](#cfn-appmesh-virtualservice-virtualserviceprovider-virtualrouter): 
    VirtualRouterServiceProvider
```

## Properties<a name="aws-properties-appmesh-virtualservice-virtualserviceprovider-properties"></a>

`VirtualNode`  <a name="cfn-appmesh-virtualservice-virtualserviceprovider-virtualnode"></a>
The virtual node associated with a virtual service\.  
*Required*: No  
*Type*: [VirtualNodeServiceProvider](aws-properties-appmesh-virtualservice-virtualnodeserviceprovider.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualRouter`  <a name="cfn-appmesh-virtualservice-virtualserviceprovider-virtualrouter"></a>
The virtual router associated with a virtual service\.  
*Required*: No  
*Type*: [VirtualRouterServiceProvider](aws-properties-appmesh-virtualservice-virtualrouterserviceprovider.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)