# AWS::AppMesh::VirtualNode VirtualServiceBackend<a name="aws-properties-appmesh-virtualnode-virtualservicebackend"></a>

An object that represents a virtual service backend for a virtual node\.

## Syntax<a name="aws-properties-appmesh-virtualnode-virtualservicebackend-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-virtualservicebackend-syntax.json"></a>

```
{
  "[ClientPolicy](#cfn-appmesh-virtualnode-virtualservicebackend-clientpolicy)" : ClientPolicy,
  "[VirtualServiceName](#cfn-appmesh-virtualnode-virtualservicebackend-virtualservicename)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-virtualservicebackend-syntax.yaml"></a>

```
  [ClientPolicy](#cfn-appmesh-virtualnode-virtualservicebackend-clientpolicy): 
    ClientPolicy
  [VirtualServiceName](#cfn-appmesh-virtualnode-virtualservicebackend-virtualservicename): String
```

## Properties<a name="aws-properties-appmesh-virtualnode-virtualservicebackend-properties"></a>

`ClientPolicy`  <a name="cfn-appmesh-virtualnode-virtualservicebackend-clientpolicy"></a>
A reference to an object that represents the client policy for a backend\.  
*Required*: No  
*Type*: [ClientPolicy](aws-properties-appmesh-virtualnode-clientpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualServiceName`  <a name="cfn-appmesh-virtualnode-virtualservicebackend-virtualservicename"></a>
The name of the virtual service that is acting as a virtual node backend\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)