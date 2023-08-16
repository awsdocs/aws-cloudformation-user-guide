# AWS::MediaConnect::Bridge BridgeSource<a name="aws-properties-mediaconnect-bridge-bridgesource"></a>

The bridge's source\. 

## Syntax<a name="aws-properties-mediaconnect-bridge-bridgesource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconnect-bridge-bridgesource-syntax.json"></a>

```
{
  "[FlowSource](#cfn-mediaconnect-bridge-bridgesource-flowsource)" : BridgeFlowSource,
  "[NetworkSource](#cfn-mediaconnect-bridge-bridgesource-networksource)" : BridgeNetworkSource
}
```

### YAML<a name="aws-properties-mediaconnect-bridge-bridgesource-syntax.yaml"></a>

```
  [FlowSource](#cfn-mediaconnect-bridge-bridgesource-flowsource): 
    BridgeFlowSource
  [NetworkSource](#cfn-mediaconnect-bridge-bridgesource-networksource): 
    BridgeNetworkSource
```

## Properties<a name="aws-properties-mediaconnect-bridge-bridgesource-properties"></a>

`FlowSource`  <a name="cfn-mediaconnect-bridge-bridgesource-flowsource"></a>
The source of the bridge\. A flow source originates in MediaConnect as an existing cloud flow\.   
*Required*: No  
*Type*: [BridgeFlowSource](aws-properties-mediaconnect-bridge-bridgeflowsource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkSource`  <a name="cfn-mediaconnect-bridge-bridgesource-networksource"></a>
The source of the bridge\. A network source originates at your premises\.   
*Required*: No  
*Type*: [BridgeNetworkSource](aws-properties-mediaconnect-bridge-bridgenetworksource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)