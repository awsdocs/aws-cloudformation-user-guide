# AWS::AppMesh::Mesh EgressFilter<a name="aws-properties-appmesh-mesh-egressfilter"></a>

An object that represents the egress filter rules for a service mesh\.

## Syntax<a name="aws-properties-appmesh-mesh-egressfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-mesh-egressfilter-syntax.json"></a>

```
{
  "[Type](#cfn-appmesh-mesh-egressfilter-type)" : String
}
```

### YAML<a name="aws-properties-appmesh-mesh-egressfilter-syntax.yaml"></a>

```
  [Type](#cfn-appmesh-mesh-egressfilter-type): String
```

## Properties<a name="aws-properties-appmesh-mesh-egressfilter-properties"></a>

`Type`  <a name="cfn-appmesh-mesh-egressfilter-type"></a>
The egress filter type\. By default, the type is `DROP_ALL`, which allows egress only from virtual nodes to other defined resources in the service mesh \(and any traffic to `*.amazonaws.com` for AWS API calls\)\. You can set the egress filter type to `ALLOW_ALL` to allow egress to any endpoint inside or outside of the service mesh\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)