# AWS::AppMesh::VirtualGateway VirtualGatewayListenerTlsFileCertificate<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertlsfilecertificate"></a>

An object that represents a local file certificate\. The certificate must meet specific requirements and you must have proxy authorization enabled\. For more information, see [Transport Layer Security \(TLS\)](https://docs.aws.amazon.com/app-mesh/latest/userguide/tls.html#virtual-node-tls-prerequisites)\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertlsfilecertificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertlsfilecertificate-syntax.json"></a>

```
{
  "[CertificateChain](#cfn-appmesh-virtualgateway-virtualgatewaylistenertlsfilecertificate-certificatechain)" : String,
  "[PrivateKey](#cfn-appmesh-virtualgateway-virtualgatewaylistenertlsfilecertificate-privatekey)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertlsfilecertificate-syntax.yaml"></a>

```
  [CertificateChain](#cfn-appmesh-virtualgateway-virtualgatewaylistenertlsfilecertificate-certificatechain): String
  [PrivateKey](#cfn-appmesh-virtualgateway-virtualgatewaylistenertlsfilecertificate-privatekey): String
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertlsfilecertificate-properties"></a>

`CertificateChain`  <a name="cfn-appmesh-virtualgateway-virtualgatewaylistenertlsfilecertificate-certificatechain"></a>
The certificate chain for the certificate\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKey`  <a name="cfn-appmesh-virtualgateway-virtualgatewaylistenertlsfilecertificate-privatekey"></a>
The private key for a certificate stored on the file system of the mesh endpoint that the proxy is running on\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)