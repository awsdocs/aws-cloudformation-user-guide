# AWS::AppMesh::VirtualNode TlsValidationContextSdsTrust<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontextsdstrust"></a>

An object that represents a Transport Layer Security \(TLS\) Secret Discovery Service validation context trust\. The proxy must be configured with a local SDS provider via a Unix Domain Socket\. See App Mesh [TLS documentation](https://docs.aws.amazon.com/app-mesh/latest/userguide/tls.html) for more info\.

## Syntax<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontextsdstrust-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontextsdstrust-syntax.json"></a>

```
{
  "[SecretName](#cfn-appmesh-virtualnode-tlsvalidationcontextsdstrust-secretname)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontextsdstrust-syntax.yaml"></a>

```
  [SecretName](#cfn-appmesh-virtualnode-tlsvalidationcontextsdstrust-secretname): String
```

## Properties<a name="aws-properties-appmesh-virtualnode-tlsvalidationcontextsdstrust-properties"></a>

`SecretName`  <a name="cfn-appmesh-virtualnode-tlsvalidationcontextsdstrust-secretname"></a>
A reference to an object that represents the name of the secret for a Transport Layer Security \(TLS\) Secret Discovery Service validation context trust\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)