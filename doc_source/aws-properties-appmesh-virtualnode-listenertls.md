# AWS::AppMesh::VirtualNode ListenerTls<a name="aws-properties-appmesh-virtualnode-listenertls"></a>

An object that represents the Transport Layer Security \(TLS\) properties for a listener\.

## Syntax<a name="aws-properties-appmesh-virtualnode-listenertls-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-listenertls-syntax.json"></a>

```
{
  "[Certificate](#cfn-appmesh-virtualnode-listenertls-certificate)" : ListenerTlsCertificate,
  "[Mode](#cfn-appmesh-virtualnode-listenertls-mode)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-listenertls-syntax.yaml"></a>

```
  [Certificate](#cfn-appmesh-virtualnode-listenertls-certificate): 
    ListenerTlsCertificate
  [Mode](#cfn-appmesh-virtualnode-listenertls-mode): String
```

## Properties<a name="aws-properties-appmesh-virtualnode-listenertls-properties"></a>

`Certificate`  <a name="cfn-appmesh-virtualnode-listenertls-certificate"></a>
A reference to an object that represents a listener's TLS certificate\.  
*Required*: Yes  
*Type*: [ListenerTlsCertificate](aws-properties-appmesh-virtualnode-listenertlscertificate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-appmesh-virtualnode-listenertls-mode"></a>
Specify one of the following modes\.  
+ ****STRICT – Listener only accepts connections with TLS enabled\. 
+ ****PERMISSIVE – Listener accepts connections with or without TLS enabled\.
+ ****DISABLED – Listener only accepts connections without TLS\. 
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)