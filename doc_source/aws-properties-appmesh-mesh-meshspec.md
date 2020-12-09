# AWS::AppMesh::Mesh MeshSpec<a name="aws-properties-appmesh-mesh-meshspec"></a>

An object that represents the specification of a service mesh\.

## Syntax<a name="aws-properties-appmesh-mesh-meshspec-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-mesh-meshspec-syntax.json"></a>

```
{
  "[EgressFilter](#cfn-appmesh-mesh-meshspec-egressfilter)" : EgressFilter
}
```

### YAML<a name="aws-properties-appmesh-mesh-meshspec-syntax.yaml"></a>

```
  [EgressFilter](#cfn-appmesh-mesh-meshspec-egressfilter): 
    EgressFilter
```

## Properties<a name="aws-properties-appmesh-mesh-meshspec-properties"></a>

`EgressFilter`  <a name="cfn-appmesh-mesh-meshspec-egressfilter"></a>
The egress filter rules for the service mesh\.  
*Required*: No  
*Type*: [EgressFilter](aws-properties-appmesh-mesh-egressfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)