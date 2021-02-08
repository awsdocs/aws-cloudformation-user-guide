# AWS::AppMesh::VirtualGateway VirtualGatewayTlsValidationContextTrust<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontexttrust"></a>

An object that represents a Transport Layer Security \(TLS\) validation context trust\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontexttrust-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontexttrust-syntax.json"></a>

```
{
  "[ACM](#cfn-appmesh-virtualgateway-virtualgatewaytlsvalidationcontexttrust-acm)" : VirtualGatewayTlsValidationContextAcmTrust,
  "[File](#cfn-appmesh-virtualgateway-virtualgatewaytlsvalidationcontexttrust-file)" : VirtualGatewayTlsValidationContextFileTrust
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontexttrust-syntax.yaml"></a>

```
  [ACM](#cfn-appmesh-virtualgateway-virtualgatewaytlsvalidationcontexttrust-acm): 
    VirtualGatewayTlsValidationContextAcmTrust
  [File](#cfn-appmesh-virtualgateway-virtualgatewaytlsvalidationcontexttrust-file): 
    VirtualGatewayTlsValidationContextFileTrust
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontexttrust-properties"></a>

`ACM`  <a name="cfn-appmesh-virtualgateway-virtualgatewaytlsvalidationcontexttrust-acm"></a>
A reference to an object that represents a TLS validation context trust for an AWS Certicate Manager \(ACM\) certificate\.  
*Required*: No  
*Type*: [VirtualGatewayTlsValidationContextAcmTrust](aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontextacmtrust.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`File`  <a name="cfn-appmesh-virtualgateway-virtualgatewaytlsvalidationcontexttrust-file"></a>
An object that represents a TLS validation context trust for a local file\.  
*Required*: No  
*Type*: [VirtualGatewayTlsValidationContextFileTrust](aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontextfiletrust.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)