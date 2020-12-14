# AWS::AppMesh::VirtualGateway VirtualGatewayBackendDefaults<a name="aws-properties-appmesh-virtualgateway-virtualgatewaybackenddefaults"></a>

An object that represents the default properties for a backend\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-virtualgatewaybackenddefaults-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-virtualgatewaybackenddefaults-syntax.json"></a>

```
{
  "[ClientPolicy](#cfn-appmesh-virtualgateway-virtualgatewaybackenddefaults-clientpolicy)" : VirtualGatewayClientPolicy
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-virtualgatewaybackenddefaults-syntax.yaml"></a>

```
  [ClientPolicy](#cfn-appmesh-virtualgateway-virtualgatewaybackenddefaults-clientpolicy): 
    VirtualGatewayClientPolicy
```

## Properties<a name="aws-properties-appmesh-virtualgateway-virtualgatewaybackenddefaults-properties"></a>

`ClientPolicy`  <a name="cfn-appmesh-virtualgateway-virtualgatewaybackenddefaults-clientpolicy"></a>
A reference to an object that represents a client policy\.  
*Required*: No  
*Type*: [VirtualGatewayClientPolicy](aws-properties-appmesh-virtualgateway-virtualgatewayclientpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)