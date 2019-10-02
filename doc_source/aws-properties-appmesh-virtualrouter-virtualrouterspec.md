# AWS::AppMesh::VirtualRouter VirtualRouterSpec<a name="aws-properties-appmesh-virtualrouter-virtualrouterspec"></a>

An object representing the specification of a virtual router\.

## Syntax<a name="aws-properties-appmesh-virtualrouter-virtualrouterspec-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualrouter-virtualrouterspec-syntax.json"></a>

```
{
  "[Listeners](#cfn-appmesh-virtualrouter-virtualrouterspec-listeners)" : [ [VirtualRouterListener](aws-properties-appmesh-virtualrouter-virtualrouterlistener.md), ... ]
}
```

### YAML<a name="aws-properties-appmesh-virtualrouter-virtualrouterspec-syntax.yaml"></a>

```
  [Listeners](#cfn-appmesh-virtualrouter-virtualrouterspec-listeners): 
    - [VirtualRouterListener](aws-properties-appmesh-virtualrouter-virtualrouterlistener.md)
```

## Properties<a name="aws-properties-appmesh-virtualrouter-virtualrouterspec-properties"></a>

`Listeners`  <a name="cfn-appmesh-virtualrouter-virtualrouterspec-listeners"></a>
The listeners that the virtual router is expected to receive inbound traffic from\. Currently only one listener is supported per virtual router\.  
*Required*: Yes  
*Type*: List of [VirtualRouterListener](aws-properties-appmesh-virtualrouter-virtualrouterlistener.md)  
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
