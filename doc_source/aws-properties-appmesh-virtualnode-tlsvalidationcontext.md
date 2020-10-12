# AWS::AppMesh::VirtualNode TlsValidationContext<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontext"></a>

An object that represents a Transport Layer Security \(TLS\) validation context\.

## Syntax<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontext-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontext-syntax.json"></a>

```
{
  "[Trust](#cfn-appmesh-virtualnode-tlsvalidationcontext-trust)" : TlsValidationContextTrust
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontext-syntax.yaml"></a>

```
  [Trust](#cfn-appmesh-virtualnode-tlsvalidationcontext-trust): 
    TlsValidationContextTrust
```

## Properties<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontext-properties"></a>

`Trust`  <a name="cfn-appmesh-virtualnode-tlsvalidationcontext-trust"></a>
A reference to an object that represents a TLS validation context trust\.  
*Required*: Yes  
*Type*: [TlsValidationContextTrust](aws-properties-appmesh-virtualnode-tlsvalidationcontexttrust.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)