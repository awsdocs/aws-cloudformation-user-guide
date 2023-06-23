# AWS::MediaConnect::Bridge BridgeOutput<a name="aws-properties-mediaconnect-bridge-bridgeoutput"></a>

The output of the bridge\. 

## Syntax<a name="aws-properties-mediaconnect-bridge-bridgeoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconnect-bridge-bridgeoutput-syntax.json"></a>

```
{
  "[NetworkOutput](#cfn-mediaconnect-bridge-bridgeoutput-networkoutput)" : BridgeNetworkOutput
}
```

### YAML<a name="aws-properties-mediaconnect-bridge-bridgeoutput-syntax.yaml"></a>

```
  [NetworkOutput](#cfn-mediaconnect-bridge-bridgeoutput-networkoutput): 
    BridgeNetworkOutput
```

## Properties<a name="aws-properties-mediaconnect-bridge-bridgeoutput-properties"></a>

`NetworkOutput`  <a name="cfn-mediaconnect-bridge-bridgeoutput-networkoutput"></a>
The output of the bridge\. A network output is delivered to your premises\.   
*Required*: No  
*Type*: [BridgeNetworkOutput](aws-properties-mediaconnect-bridge-bridgenetworkoutput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)