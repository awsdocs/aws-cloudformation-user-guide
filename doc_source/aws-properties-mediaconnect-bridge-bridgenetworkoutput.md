# AWS::MediaConnect::Bridge BridgeNetworkOutput<a name="aws-properties-mediaconnect-bridge-bridgenetworkoutput"></a>

The output of the bridge\. A network output is delivered to your premises\. 

## Syntax<a name="aws-properties-mediaconnect-bridge-bridgenetworkoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconnect-bridge-bridgenetworkoutput-syntax.json"></a>

```
{
  "[IpAddress](#cfn-mediaconnect-bridge-bridgenetworkoutput-ipaddress)" : String,
  "[Name](#cfn-mediaconnect-bridge-bridgenetworkoutput-name)" : String,
  "[NetworkName](#cfn-mediaconnect-bridge-bridgenetworkoutput-networkname)" : String,
  "[Port](#cfn-mediaconnect-bridge-bridgenetworkoutput-port)" : Integer,
  "[Protocol](#cfn-mediaconnect-bridge-bridgenetworkoutput-protocol)" : String,
  "[Ttl](#cfn-mediaconnect-bridge-bridgenetworkoutput-ttl)" : Integer
}
```

### YAML<a name="aws-properties-mediaconnect-bridge-bridgenetworkoutput-syntax.yaml"></a>

```
  [IpAddress](#cfn-mediaconnect-bridge-bridgenetworkoutput-ipaddress): String
  [Name](#cfn-mediaconnect-bridge-bridgenetworkoutput-name): String
  [NetworkName](#cfn-mediaconnect-bridge-bridgenetworkoutput-networkname): String
  [Port](#cfn-mediaconnect-bridge-bridgenetworkoutput-port): Integer
  [Protocol](#cfn-mediaconnect-bridge-bridgenetworkoutput-protocol): String
  [Ttl](#cfn-mediaconnect-bridge-bridgenetworkoutput-ttl): Integer
```

## Properties<a name="aws-properties-mediaconnect-bridge-bridgenetworkoutput-properties"></a>

`IpAddress`  <a name="cfn-mediaconnect-bridge-bridgenetworkoutput-ipaddress"></a>
The network output IP Address\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mediaconnect-bridge-bridgenetworkoutput-name"></a>
The network output name\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkName`  <a name="cfn-mediaconnect-bridge-bridgenetworkoutput-networkname"></a>
The network output's gateway network name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-mediaconnect-bridge-bridgenetworkoutput-port"></a>
The network output port\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-mediaconnect-bridge-bridgenetworkoutput-protocol"></a>
The network output protocol\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ttl`  <a name="cfn-mediaconnect-bridge-bridgenetworkoutput-ttl"></a>
The network output TTL\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)