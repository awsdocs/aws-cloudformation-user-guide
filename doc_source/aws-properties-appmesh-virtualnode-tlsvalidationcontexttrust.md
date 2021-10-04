# AWS::AppMesh::VirtualNode TlsValidationContextTrust<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontexttrust"></a>

An object that represents a Transport Layer Security \(TLS\) validation context trust\.

## Syntax<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontexttrust-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontexttrust-syntax.json"></a>

```
{
  "[ACM](#cfn-appmesh-virtualnode-tlsvalidationcontexttrust-acm)" : TlsValidationContextAcmTrust,
  "[File](#cfn-appmesh-virtualnode-tlsvalidationcontexttrust-file)" : TlsValidationContextFileTrust,
  "[SDS](#cfn-appmesh-virtualnode-tlsvalidationcontexttrust-sds)" : TlsValidationContextSdsTrust
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontexttrust-syntax.yaml"></a>

```
  [ACM](#cfn-appmesh-virtualnode-tlsvalidationcontexttrust-acm): 
    TlsValidationContextAcmTrust
  [File](#cfn-appmesh-virtualnode-tlsvalidationcontexttrust-file): 
    TlsValidationContextFileTrust
  [SDS](#cfn-appmesh-virtualnode-tlsvalidationcontexttrust-sds): 
    TlsValidationContextSdsTrust
```

## Properties<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontexttrust-properties"></a>

`ACM`  <a name="cfn-appmesh-virtualnode-tlsvalidationcontexttrust-acm"></a>
A reference to an object that represents a Transport Layer Security \(TLS\) validation context trust for an AWS Certificate Manager certificate\.  
*Required*: No  
*Type*: [TlsValidationContextAcmTrust](aws-properties-appmesh-virtualnode-tlsvalidationcontextacmtrust.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`File`  <a name="cfn-appmesh-virtualnode-tlsvalidationcontexttrust-file"></a>
An object that represents a Transport Layer Security \(TLS\) validation context trust for a local file\.  
*Required*: No  
*Type*: [TlsValidationContextFileTrust](aws-properties-appmesh-virtualnode-tlsvalidationcontextfiletrust.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SDS`  <a name="cfn-appmesh-virtualnode-tlsvalidationcontexttrust-sds"></a>
A reference to an object that represents a Transport Layer Security \(TLS\) Secret Discovery Service validation context trust\.  
*Required*: No  
*Type*: [TlsValidationContextSdsTrust](aws-properties-appmesh-virtualnode-tlsvalidationcontextsdstrust.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)