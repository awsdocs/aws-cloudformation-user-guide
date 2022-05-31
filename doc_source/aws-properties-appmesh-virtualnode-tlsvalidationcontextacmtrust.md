# AWS::AppMesh::VirtualNode TlsValidationContextAcmTrust<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontextacmtrust"></a>

An object that represents a Transport Layer Security \(TLS\) validation context trust for an AWS Certificate Manager certificate\.

## Syntax<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontextacmtrust-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontextacmtrust-syntax.json"></a>

```
{
  "[CertificateAuthorityArns](#cfn-appmesh-virtualnode-tlsvalidationcontextacmtrust-certificateauthorityarns)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontextacmtrust-syntax.yaml"></a>

```
  [CertificateAuthorityArns](#cfn-appmesh-virtualnode-tlsvalidationcontextacmtrust-certificateauthorityarns): 
    - String
```

## Properties<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontextacmtrust-properties"></a>

`CertificateAuthorityArns`  <a name="cfn-appmesh-virtualnode-tlsvalidationcontextacmtrust-certificateauthorityarns"></a>
One or more ACM Amazon Resource Name \(ARN\)s\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)