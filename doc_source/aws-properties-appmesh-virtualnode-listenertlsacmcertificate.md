# AWS::AppMesh::VirtualNode ListenerTlsAcmCertificate<a name="aws-properties-appmesh-virtualnode-listenertlsacmcertificate"></a>

An object that represents an AWS Certicate Manager \(ACM\) certificate\.

## Syntax<a name="aws-properties-appmesh-virtualnode-listenertlsacmcertificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-listenertlsacmcertificate-syntax.json"></a>

```
{
  "[CertificateArn](#cfn-appmesh-virtualnode-listenertlsacmcertificate-certificatearn)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-listenertlsacmcertificate-syntax.yaml"></a>

```
  [CertificateArn](#cfn-appmesh-virtualnode-listenertlsacmcertificate-certificatearn): String
```

## Properties<a name="aws-properties-appmesh-virtualnode-listenertlsacmcertificate-properties"></a>

`CertificateArn`  <a name="cfn-appmesh-virtualnode-listenertlsacmcertificate-certificatearn"></a>
The Amazon Resource Name \(ARN\) for the certificate\. The certificate must meet specific requirements and you must have proxy authorization enabled\. For more information, see [Transport Layer Security \(TLS\)](https://docs.aws.amazon.com/app-mesh/latest/userguide/tls.html#virtual-node-tls-prerequisites)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)