# AWS::EC2::TransitGatewayConnect TransitGatewayConnectOptions<a name="aws-properties-ec2-transitgatewayconnect-transitgatewayconnectoptions"></a>

Describes the Connect attachment options\.

## Syntax<a name="aws-properties-ec2-transitgatewayconnect-transitgatewayconnectoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-transitgatewayconnect-transitgatewayconnectoptions-syntax.json"></a>

```
{
  "[Protocol](#cfn-ec2-transitgatewayconnect-transitgatewayconnectoptions-protocol)" : String
}
```

### YAML<a name="aws-properties-ec2-transitgatewayconnect-transitgatewayconnectoptions-syntax.yaml"></a>

```
  [Protocol](#cfn-ec2-transitgatewayconnect-transitgatewayconnectoptions-protocol): String
```

## Properties<a name="aws-properties-ec2-transitgatewayconnect-transitgatewayconnectoptions-properties"></a>

`Protocol`  <a name="cfn-ec2-transitgatewayconnect-transitgatewayconnectoptions-protocol"></a>
The tunnel protocol\.  
*Required*: No  
*Type*: String  
*Allowed values*: `gre`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)