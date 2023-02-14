# AWS::AppMesh::VirtualNode ListenerTlsSdsCertificate<a name="aws-properties-appmesh-virtualnode-listenertlssdscertificate"></a>

An object that represents the listener's Secret Discovery Service certificate\. The proxy must be configured with a local SDS provider via a Unix Domain Socket\. See App Mesh [TLS documentation](https://docs.aws.amazon.com/app-mesh/latest/userguide/tls.html) for more info\.

## Syntax<a name="aws-properties-appmesh-virtualnode-listenertlssdscertificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-listenertlssdscertificate-syntax.json"></a>

```
{
  "[SecretName](#cfn-appmesh-virtualnode-listenertlssdscertificate-secretname)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-listenertlssdscertificate-syntax.yaml"></a>

```
  [SecretName](#cfn-appmesh-virtualnode-listenertlssdscertificate-secretname): String
```

## Properties<a name="aws-properties-appmesh-virtualnode-listenertlssdscertificate-properties"></a>

`SecretName`  <a name="cfn-appmesh-virtualnode-listenertlssdscertificate-secretname"></a>
A reference to an object that represents the name of the secret requested from the Secret Discovery Service provider representing Transport Layer Security \(TLS\) materials like a certificate or certificate chain\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)