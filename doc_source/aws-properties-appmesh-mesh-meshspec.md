# AWS::AppMesh::Mesh MeshSpec<a name="aws-properties-appmesh-mesh-meshspec"></a>

An object representing the specification of a service mesh\.

## Syntax<a name="aws-properties-appmesh-mesh-meshspec-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-mesh-meshspec-syntax.json"></a>

```
{
  "[EgressFilter](#cfn-appmesh-mesh-meshspec-egressfilter)" : [EgressFilter](aws-properties-appmesh-mesh-egressfilter.md)
}
```

### YAML<a name="aws-properties-appmesh-mesh-meshspec-syntax.yaml"></a>

```
  [EgressFilter](#cfn-appmesh-mesh-meshspec-egressfilter): 
    [EgressFilter](aws-properties-appmesh-mesh-egressfilter.md)
```

## Properties<a name="aws-properties-appmesh-mesh-meshspec-properties"></a>

`EgressFilter`  <a name="cfn-appmesh-mesh-meshspec-egressfilter"></a>
The egress filter rules for the service mesh\.  
*Required*: No  
*Type*: [EgressFilter](aws-properties-appmesh-mesh-egressfilter.md)  
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
