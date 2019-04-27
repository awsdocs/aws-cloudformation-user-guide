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
﻿  [PortMapping](#cfn-appmesh-virtualrouter-virtualrouterlistener-portmapping) : [PortMapping](aws-properties-appmesh-virtualrouter-portmapping.md)
```

## Properties<a name="aws-properties-appmesh-virtualrouter-virtualrouterlistener-properties"></a>

`PortMapping`  <a name="cfn-appmesh-virtualrouter-virtualrouterlistener-portmapping"></a>
The port mapping information for the listener\.  
*Required*: Yes  
*Type*: [PortMapping](aws-properties-appmesh-virtualrouter-portmapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)