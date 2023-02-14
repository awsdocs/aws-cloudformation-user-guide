# AWS::AppMesh::VirtualGateway VirtualGatewayClientPolicy<a name="aws-properties-appmesh-virtualgateway-virtualgatewayclientpolicy"></a>

An object that represents a client policy\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewayclientpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewayclientpolicy-syntax.json"></a>

```
{
  "[TLS](#cfn-appmesh-virtualgateway-virtualgatewayclientpolicy-tls)" : VirtualGatewayClientPolicyTls
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewayclientpolicy-syntax.yaml"></a>

```
  [TLS](#cfn-appmesh-virtualgateway-virtualgatewayclientpolicy-tls): 
    VirtualGatewayClientPolicyTls
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewayclientpolicy-properties"></a>

`TLS`  <a name="cfn-appmesh-virtualgateway-virtualgatewayclientpolicy-tls"></a>
A reference to an object that represents a Transport Layer Security \(TLS\) client policy\.  
*Required*: No  
*Type*: [VirtualGatewayClientPolicyTls](aws-properties-appmesh-virtualgateway-virtualgatewayclientpolicytls.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)