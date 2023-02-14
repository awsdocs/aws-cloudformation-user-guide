# AWS::AppMesh::VirtualGateway VirtualGatewayListenerTlsValidationContextTrust<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertlsvalidationcontexttrust"></a>

An object that represents a virtual gateway's listener's Transport Layer Security \(TLS\) validation context trust\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertlsvalidationcontexttrust-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertlsvalidationcontexttrust-syntax.json"></a>

```
{
  "[File](#cfn-appmesh-virtualgateway-virtualgatewaylistenertlsvalidationcontexttrust-file)" : VirtualGatewayTlsValidationContextFileTrust,
  "[SDS](#cfn-appmesh-virtualgateway-virtualgatewaylistenertlsvalidationcontexttrust-sds)" : VirtualGatewayTlsValidationContextSdsTrust
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertlsvalidationcontexttrust-syntax.yaml"></a>

```
  [File](#cfn-appmesh-virtualgateway-virtualgatewaylistenertlsvalidationcontexttrust-file): 
    VirtualGatewayTlsValidationContextFileTrust
  [SDS](#cfn-appmesh-virtualgateway-virtualgatewaylistenertlsvalidationcontexttrust-sds): 
    VirtualGatewayTlsValidationContextSdsTrust
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertlsvalidationcontexttrust-properties"></a>

`File`  <a name="cfn-appmesh-virtualgateway-virtualgatewaylistenertlsvalidationcontexttrust-file"></a>
An object that represents a Transport Layer Security \(TLS\) validation context trust for a local file\.  
*Required*: No  
*Type*: [VirtualGatewayTlsValidationContextFileTrust](aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontextfiletrust.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SDS`  <a name="cfn-appmesh-virtualgateway-virtualgatewaylistenertlsvalidationcontexttrust-sds"></a>
A reference to an object that represents a virtual gateway's listener's Transport Layer Security \(TLS\) Secret Discovery Service validation context trust\.  
*Required*: No  
*Type*: [VirtualGatewayTlsValidationContextSdsTrust](aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontextsdstrust.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)