# AWS::AppMesh::VirtualNode Backend<a name="aws-properties-appmesh-virtualnode-backend"></a>

An object representing the backends that a virtual node is expected to send outbound traffic to\. 

## Syntax<a name="aws-properties-appmesh-virtualnode-backend-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-backend-syntax.json"></a>

```
{
  "[VirtualService](#cfn-appmesh-virtualnode-backend-virtualservice)" : [VirtualServiceBackend](aws-properties-appmesh-virtualnode-virtualservicebackend.md)
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-backend-syntax.yaml"></a>

```
  [VirtualService](#cfn-appmesh-virtualnode-backend-virtualservice): 
    [VirtualServiceBackend](aws-properties-appmesh-virtualnode-virtualservicebackend.md)
```

## Properties<a name="aws-properties-appmesh-virtualnode-backend-properties"></a>

`VirtualService`  <a name="cfn-appmesh-virtualnode-backend-virtualservice"></a>
Specifies a virtual service to use as a backend for a virtual node\.   
*Required*: No  
*Type*: [VirtualServiceBackend](aws-properties-appmesh-virtualnode-virtualservicebackend.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)