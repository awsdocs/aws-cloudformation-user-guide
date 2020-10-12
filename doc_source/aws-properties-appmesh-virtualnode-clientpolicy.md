# AWS::AppMesh::VirtualNode ClientPolicy<a name="aws-properties-appmesh-virtualnode-clientpolicy"></a>

An object that represents a client policy\.

## Syntax<a name="aws-properties-appmesh-virtualnode-clientpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-clientpolicy-syntax.json"></a>

```
{
  "[TLS](#cfn-appmesh-virtualnode-clientpolicy-tls)" : ClientPolicyTls
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-clientpolicy-syntax.yaml"></a>

```
  [TLS](#cfn-appmesh-virtualnode-clientpolicy-tls): 
    ClientPolicyTls
```

## Properties<a name="aws-properties-appmesh-virtualnode-clientpolicy-properties"></a>

`TLS`  <a name="cfn-appmesh-virtualnode-clientpolicy-tls"></a>
A reference to an object that represents a Transport Layer Security \(TLS\) client policy\.  
*Required*: No  
*Type*: [ClientPolicyTls](aws-properties-appmesh-virtualnode-clientpolicytls.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)