# AWS::AppMesh::VirtualService VirtualServiceSpec<a name="aws-properties-appmesh-virtualservice-virtualservicespec"></a>

An object representing the specification of a virtual service\.

## Syntax<a name="aws-properties-appmesh-virtualservice-virtualservicespec-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualservice-virtualservicespec-syntax.json"></a>

```
{
  "[Provider](#cfn-appmesh-virtualservice-virtualservicespec-provider)" : [VirtualServiceProvider](aws-properties-appmesh-virtualservice-virtualserviceprovider.md)
}
```

### YAML<a name="aws-properties-appmesh-virtualservice-virtualservicespec-syntax.yaml"></a>

```
  [Provider](#cfn-appmesh-virtualservice-virtualservicespec-provider): 
    [VirtualServiceProvider](aws-properties-appmesh-virtualservice-virtualserviceprovider.md)
```

## Properties<a name="aws-properties-appmesh-virtualservice-virtualservicespec-properties"></a>

`Provider`  <a name="cfn-appmesh-virtualservice-virtualservicespec-provider"></a>
The App Mesh object that is acting as the provider for a virtual service\. You can specify a single virtual node or virtual router\.  
*Required*: No  
*Type*: [VirtualServiceProvider](aws-properties-appmesh-virtualservice-virtualserviceprovider.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
