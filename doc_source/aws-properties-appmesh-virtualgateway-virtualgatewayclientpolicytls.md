# AWS::AppMesh::VirtualGateway VirtualGatewayClientPolicyTls<a name="aws-properties-appmesh-virtualgateway-virtualgatewayclientpolicytls"></a>

An object that represents a Transport Layer Security \(TLS\) client policy\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewayclientpolicytls-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewayclientpolicytls-syntax.json"></a>

```
{
  "[Enforce](#cfn-appmesh-virtualgateway-virtualgatewayclientpolicytls-enforce)" : Boolean,
  "[Ports](#cfn-appmesh-virtualgateway-virtualgatewayclientpolicytls-ports)" : [ Integer, ... ],
  "[Validation](#cfn-appmesh-virtualgateway-virtualgatewayclientpolicytls-validation)" : VirtualGatewayTlsValidationContext
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewayclientpolicytls-syntax.yaml"></a>

```
  [Enforce](#cfn-appmesh-virtualgateway-virtualgatewayclientpolicytls-enforce): Boolean
  [Ports](#cfn-appmesh-virtualgateway-virtualgatewayclientpolicytls-ports): 
    - Integer
  [Validation](#cfn-appmesh-virtualgateway-virtualgatewayclientpolicytls-validation): 
    VirtualGatewayTlsValidationContext
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewayclientpolicytls-properties"></a>

`Enforce`  <a name="cfn-appmesh-virtualgateway-virtualgatewayclientpolicytls-enforce"></a>
Whether the policy is enforced\. The default is `True`, if a value isn't specified\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ports`  <a name="cfn-appmesh-virtualgateway-virtualgatewayclientpolicytls-ports"></a>
One or more ports that the policy is enforced for\.  
*Required*: No  
*Type*: List of Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Validation`  <a name="cfn-appmesh-virtualgateway-virtualgatewayclientpolicytls-validation"></a>
A reference to an object that represents a TLS validation context\.  
*Required*: Yes  
*Type*: [VirtualGatewayTlsValidationContext](aws-properties-appmesh-virtualgateway-virtualgatewaytlsvalidationcontext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)