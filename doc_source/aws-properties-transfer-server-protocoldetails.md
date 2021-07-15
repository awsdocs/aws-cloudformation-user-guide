# AWS::Transfer::Server ProtocolDetails<a name="aws-properties-transfer-server-protocoldetails"></a>

Protocol settings that are configured for your server\.

## Syntax<a name="aws-properties-transfer-server-protocoldetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-server-protocoldetails-syntax.json"></a>

```
{
  "[PassiveIp](#cfn-transfer-server-protocoldetails-passiveip)" : String
}
```

### YAML<a name="aws-properties-transfer-server-protocoldetails-syntax.yaml"></a>

```
  [PassiveIp](#cfn-transfer-server-protocoldetails-passiveip): String
```

## Properties<a name="aws-properties-transfer-server-protocoldetails-properties"></a>

`PassiveIp`  <a name="cfn-transfer-server-protocoldetails-passiveip"></a>
 Indicates passive mode, for FTP and FTPS protocols\. Enter a single dotted\-quad IPv4 address, such as the external IP address of a firewall, router, or load balancer\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)