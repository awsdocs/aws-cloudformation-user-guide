# AWS::AppMesh::Mesh MeshServiceDiscovery<a name="aws-properties-appmesh-mesh-meshservicediscovery"></a>

An object that represents the service discovery information for a service mesh\.

## Syntax<a name="aws-properties-appmesh-mesh-meshservicediscovery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-mesh-meshservicediscovery-syntax.json"></a>

```
{
  "[IpPreference](#cfn-appmesh-mesh-meshservicediscovery-ippreference)" : String
}
```

### YAML<a name="aws-properties-appmesh-mesh-meshservicediscovery-syntax.yaml"></a>

```
  [IpPreference](#cfn-appmesh-mesh-meshservicediscovery-ippreference): String
```

## Properties<a name="aws-properties-appmesh-mesh-meshservicediscovery-properties"></a>

`IpPreference`  <a name="cfn-appmesh-mesh-meshservicediscovery-ippreference"></a>
The IP version to use to control traffic within the mesh\.  
*Required*: No  
*Type*: String  
*Allowed values*: `IPv4_ONLY | IPv4_PREFERRED | IPv6_ONLY | IPv6_PREFERRED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)