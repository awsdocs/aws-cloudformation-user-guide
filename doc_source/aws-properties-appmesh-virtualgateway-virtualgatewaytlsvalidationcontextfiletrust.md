# AWS::AppMesh::VirtualGateway VirtualGatewayTlsValidationContextFileTrust<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontextfiletrust"></a>

An object that represents a Transport Layer Security \(TLS\) validation context trust for a local file\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontextfiletrust-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontextfiletrust-syntax.json"></a>

```
{
  "[CertificateChain](#cfn-appmesh-virtualgateway-virtualgatewaytlsvalidationcontextfiletrust-certificatechain)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontextfiletrust-syntax.yaml"></a>

```
  [CertificateChain](#cfn-appmesh-virtualgateway-virtualgatewaytlsvalidationcontextfiletrust-certificatechain): String
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontextfiletrust-properties"></a>

`CertificateChain`  <a name="cfn-appmesh-virtualgateway-virtualgatewaytlsvalidationcontextfiletrust-certificatechain"></a>
The certificate trust chain for a certificate stored on the file system of the virtual node that the proxy is running on\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)