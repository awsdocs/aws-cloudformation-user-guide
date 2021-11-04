# AWS::AppMesh::VirtualGateway VirtualGatewayListenerTls<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertls"></a>

An object that represents the Transport Layer Security \(TLS\) properties for a listener\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertls-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertls-syntax.json"></a>

```
{
  "[Certificate](#cfn-appmesh-virtualgateway-virtualgatewaylistenertls-certificate)" : VirtualGatewayListenerTlsCertificate,
  "[Mode](#cfn-appmesh-virtualgateway-virtualgatewaylistenertls-mode)" : String,
  "[Validation](#cfn-appmesh-virtualgateway-virtualgatewaylistenertls-validation)" : VirtualGatewayListenerTlsValidationContext
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertls-syntax.yaml"></a>

```
  [Certificate](#cfn-appmesh-virtualgateway-virtualgatewaylistenertls-certificate): 
    VirtualGatewayListenerTlsCertificate
  [Mode](#cfn-appmesh-virtualgateway-virtualgatewaylistenertls-mode): String
  [Validation](#cfn-appmesh-virtualgateway-virtualgatewaylistenertls-validation): 
    VirtualGatewayListenerTlsValidationContext
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewaylistenertls-properties"></a>

`Certificate`  <a name="cfn-appmesh-virtualgateway-virtualgatewaylistenertls-certificate"></a>
An object that represents a Transport Layer Security \(TLS\) certificate\.  
*Required*: Yes  
*Type*: [VirtualGatewayListenerTlsCertificate](aws-properties-appmesh-virtualgateway-virtualgatewaylistenertlscertificate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-appmesh-virtualgateway-virtualgatewaylistenertls-mode"></a>
Specify one of the following modes\.  
+ ****STRICT – Listener only accepts connections with TLS enabled\. 
+ ****PERMISSIVE – Listener accepts connections with or without TLS enabled\.
+ ****DISABLED – Listener only accepts connections without TLS\. 
*Required*: Yes  
*Type*: String  
*Allowed values*: `DISABLED | PERMISSIVE | STRICT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Validation`  <a name="cfn-appmesh-virtualgateway-virtualgatewaylistenertls-validation"></a>
A reference to an object that represents a virtual gateway's listener's Transport Layer Security \(TLS\) validation context\.  
*Required*: No  
*Type*: [VirtualGatewayListenerTlsValidationContext](aws-properties-appmesh-virtualgateway-virtualgatewaylistenertlsvalidationcontext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)