# AWS::AppMesh::VirtualGateway VirtualGatewayTlsValidationContext<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontext"></a>

An object that represents a Transport Layer Security \(TLS\) validation context\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontext-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontext-syntax.json"></a>

```
{
  "[Trust](#cfn-appmesh-virtualgateway-virtualgatewaytlsvalidationcontext-trust)" : VirtualGatewayTlsValidationContextTrust
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontext-syntax.yaml"></a>

```
  [Trust](#cfn-appmesh-virtualgateway-virtualgatewaytlsvalidationcontext-trust): 
    VirtualGatewayTlsValidationContextTrust
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontext-properties"></a>

`Trust`  <a name="cfn-appmesh-virtualgateway-virtualgatewaytlsvalidationcontext-trust"></a>
A reference to an object that represents a TLS validation context trust\.  
*Required*: Yes  
*Type*: [VirtualGatewayTlsValidationContextTrust](aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontexttrust.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)