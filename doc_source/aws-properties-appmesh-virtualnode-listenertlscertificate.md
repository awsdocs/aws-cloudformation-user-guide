# AWS::AppMesh::VirtualNode ListenerTlsCertificate<a name="aws-properties-appmesh-virtualnode-listenertlscertificate"></a>

An object that represents a listener's Transport Layer Security \(TLS\) certificate\.

## Syntax<a name="aws-properties-appmesh-virtualnode-listenertlscertificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-listenertlscertificate-syntax.json"></a>

```
{
  "[ACM](#cfn-appmesh-virtualnode-listenertlscertificate-acm)" : ListenerTlsAcmCertificate,
  "[File](#cfn-appmesh-virtualnode-listenertlscertificate-file)" : ListenerTlsFileCertificate,
  "[SDS](#cfn-appmesh-virtualnode-listenertlscertificate-sds)" : ListenerTlsSdsCertificate
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-listenertlscertificate-syntax.yaml"></a>

```
  [ACM](#cfn-appmesh-virtualnode-listenertlscertificate-acm): 
    ListenerTlsAcmCertificate
  [File](#cfn-appmesh-virtualnode-listenertlscertificate-file): 
    ListenerTlsFileCertificate
  [SDS](#cfn-appmesh-virtualnode-listenertlscertificate-sds): 
    ListenerTlsSdsCertificate
```

## Properties<a name="aws-properties-appmesh-virtualnode-listenertlscertificate-properties"></a>

`ACM`  <a name="cfn-appmesh-virtualnode-listenertlscertificate-acm"></a>
A reference to an object that represents an AWS Certificate Manager certificate\.  
*Required*: No  
*Type*: [ListenerTlsAcmCertificate](aws-properties-appmesh-virtualnode-listenertlsacmcertificate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`File`  <a name="cfn-appmesh-virtualnode-listenertlscertificate-file"></a>
A reference to an object that represents a local file certificate\.  
*Required*: No  
*Type*: [ListenerTlsFileCertificate](aws-properties-appmesh-virtualnode-listenertlsfilecertificate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SDS`  <a name="cfn-appmesh-virtualnode-listenertlscertificate-sds"></a>
A reference to an object that represents a listener's Secret Discovery Service certificate\.  
*Required*: No  
*Type*: [ListenerTlsSdsCertificate](aws-properties-appmesh-virtualnode-listenertlssdscertificate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)