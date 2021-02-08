# AWS::AppMesh::VirtualNode ClientPolicyTls<a name="aws-properties-appmesh-virtualnode-clientpolicytls"></a>

A reference to an object that represents a Transport Layer Security \(TLS\) client policy\.

## Syntax<a name="aws-properties-appmesh-virtualnode-clientpolicytls-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-clientpolicytls-syntax.json"></a>

```
{
  "[Enforce](#cfn-appmesh-virtualnode-clientpolicytls-enforce)" : Boolean,
  "[Ports](#cfn-appmesh-virtualnode-clientpolicytls-ports)" : [ Integer, ... ],
  "[Validation](#cfn-appmesh-virtualnode-clientpolicytls-validation)" : TlsValidationContext
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-clientpolicytls-syntax.yaml"></a>

```
  [Enforce](#cfn-appmesh-virtualnode-clientpolicytls-enforce): Boolean
  [Ports](#cfn-appmesh-virtualnode-clientpolicytls-ports): 
    - Integer
  [Validation](#cfn-appmesh-virtualnode-clientpolicytls-validation): 
    TlsValidationContext
```

## Properties<a name="aws-properties-appmesh-virtualnode-clientpolicytls-properties"></a>

`Enforce`  <a name="cfn-appmesh-virtualnode-clientpolicytls-enforce"></a>
Whether the policy is enforced\. The default is `True`, if a value isn't specified\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ports`  <a name="cfn-appmesh-virtualnode-clientpolicytls-ports"></a>
One or more ports that the policy is enforced for\.  
*Required*: No  
*Type*: List of Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Validation`  <a name="cfn-appmesh-virtualnode-clientpolicytls-validation"></a>
A reference to an object that represents a TLS validation context\.  
*Required*: Yes  
*Type*: [TlsValidationContext](aws-properties-appmesh-virtualnode-tlsvalidationcontext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)