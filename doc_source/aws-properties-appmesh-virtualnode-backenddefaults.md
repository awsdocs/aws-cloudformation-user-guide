# AWS::AppMesh::VirtualNode BackendDefaults<a name="aws-properties-appmesh-virtualnode-backenddefaults"></a>

An object that represents the default properties for a backend\.

## Syntax<a name="aws-properties-appmesh-virtualnode-backenddefaults-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-backenddefaults-syntax.json"></a>

```
{
  "[ClientPolicy](#cfn-appmesh-virtualnode-backenddefaults-clientpolicy)" : ClientPolicy
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-backenddefaults-syntax.yaml"></a>

```
  [ClientPolicy](#cfn-appmesh-virtualnode-backenddefaults-clientpolicy): 
    ClientPolicy
```

## Properties<a name="aws-properties-appmesh-virtualnode-backenddefaults-properties"></a>

`ClientPolicy`  <a name="cfn-appmesh-virtualnode-backenddefaults-clientpolicy"></a>
A reference to an object that represents a client policy\.  
*Required*: No  
*Type*: [ClientPolicy](aws-properties-appmesh-virtualnode-clientpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)