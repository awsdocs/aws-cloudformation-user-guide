# AWS::AppMesh::VirtualNode ListenerTlsFileCertificate<a name="aws-properties-appmesh-virtualnode-listenertlsfilecertificate"></a>

An object that represents a local file certificate\. The certificate must meet specific requirements and you must have proxy authorization enabled\. For more information, see [Transport Layer Security \(TLS\)](https://docs.aws.amazon.com/app-mesh/latest/userguide/tls.html#virtual-node-tls-prerequisites)\.

## Syntax<a name="aws-properties-appmesh-virtualnode-listenertlsfilecertificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-listenertlsfilecertificate-syntax.json"></a>

```
{
  "[CertificateChain](#cfn-appmesh-virtualnode-listenertlsfilecertificate-certificatechain)" : String,
  "[PrivateKey](#cfn-appmesh-virtualnode-listenertlsfilecertificate-privatekey)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-listenertlsfilecertificate-syntax.yaml"></a>

```
  [CertificateChain](#cfn-appmesh-virtualnode-listenertlsfilecertificate-certificatechain): String
  [PrivateKey](#cfn-appmesh-virtualnode-listenertlsfilecertificate-privatekey): String
```

## Properties<a name="aws-properties-appmesh-virtualnode-listenertlsfilecertificate-properties"></a>

`CertificateChain`  <a name="cfn-appmesh-virtualnode-listenertlsfilecertificate-certificatechain"></a>
The certificate chain for the certificate\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKey`  <a name="cfn-appmesh-virtualnode-listenertlsfilecertificate-privatekey"></a>
The private key for a certificate stored on the file system of the virtual node that the proxy is running on\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)