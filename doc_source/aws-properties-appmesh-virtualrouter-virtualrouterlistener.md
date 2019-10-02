# AWS::AppMesh::VirtualRouter VirtualRouterListener<a name="aws-properties-appmesh-virtualrouter-virtualrouterlistener"></a>

An object representing a virtual router listener\.

## Syntax<a name="aws-properties-appmesh-virtualrouter-virtualrouterlistener-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualrouter-virtualrouterlistener-syntax.json"></a>

```
{
  "[PortMapping](#cfn-appmesh-virtualrouter-virtualrouterlistener-portmapping)" : [PortMapping](aws-properties-appmesh-virtualrouter-portmapping.md)
}
```

### YAML<a name="aws-properties-appmesh-virtualrouter-virtualrouterlistener-syntax.yaml"></a>

```
  [PortMapping](#cfn-appmesh-virtualrouter-virtualrouterlistener-portmapping): 
    [PortMapping](aws-properties-appmesh-virtualrouter-portmapping.md)
```

## Properties<a name="aws-properties-appmesh-virtualrouter-virtualrouterlistener-properties"></a>

`PortMapping`  <a name="cfn-appmesh-virtualrouter-virtualrouterlistener-portmapping"></a>
The port mapping information for the listener\.  
*Required*: Yes  
*Type*: [PortMapping](aws-properties-appmesh-virtualrouter-portmapping.md)  
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
