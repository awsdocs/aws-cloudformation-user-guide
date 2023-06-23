# AWS::MediaConnect::BridgeSource<a name="aws-resource-mediaconnect-bridgesource"></a>

Adds sources to an existing bridge\.

## Syntax<a name="aws-resource-mediaconnect-bridgesource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediaconnect-bridgesource-syntax.json"></a>

```
{
  "Type" : "AWS::MediaConnect::BridgeSource",
  "Properties" : {
      "[BridgeArn](#cfn-mediaconnect-bridgesource-bridgearn)" : String,
      "[FlowSource](#cfn-mediaconnect-bridgesource-flowsource)" : BridgeFlowSource,
      "[Name](#cfn-mediaconnect-bridgesource-name)" : String,
      "[NetworkSource](#cfn-mediaconnect-bridgesource-networksource)" : BridgeNetworkSource
    }
}
```

### YAML<a name="aws-resource-mediaconnect-bridgesource-syntax.yaml"></a>

```
Type: AWS::MediaConnect::BridgeSource
Properties: 
  [BridgeArn](#cfn-mediaconnect-bridgesource-bridgearn): String
  [FlowSource](#cfn-mediaconnect-bridgesource-flowsource): 
    BridgeFlowSource
  [Name](#cfn-mediaconnect-bridgesource-name): String
  [NetworkSource](#cfn-mediaconnect-bridgesource-networksource): 
    BridgeNetworkSource
```

## Properties<a name="aws-resource-mediaconnect-bridgesource-properties"></a>

`BridgeArn`  <a name="cfn-mediaconnect-bridgesource-bridgearn"></a>
The ARN of the bridge that you want to describe\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FlowSource`  <a name="cfn-mediaconnect-bridgesource-flowsource"></a>
Add a flow source to an existing bridge\.  
*Required*: No  
*Type*: [BridgeFlowSource](aws-properties-mediaconnect-bridgesource-bridgeflowsource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mediaconnect-bridgesource-name"></a>
The name of the network source\. This name is used to reference the source and must be unique among sources in this bridge\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkSource`  <a name="cfn-mediaconnect-bridgesource-networksource"></a>
Add a network source to an existing bridge\.  
*Required*: No  
*Type*: [BridgeNetworkSource](aws-properties-mediaconnect-bridgesource-bridgenetworksource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediaconnect-bridgesource-return-values"></a>

### Ref<a name="aws-resource-mediaconnect-bridgesource-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the bridge ARN and bridge name\. For example:

`{ "Ref": "arn:aws:mediaconnect:us-east-1:111122223333:bridge:1-23aBC45dEF67hiJ8-12AbC34DE5fG:BasketballArenaIngress|Source:PrimarySource1" }`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.