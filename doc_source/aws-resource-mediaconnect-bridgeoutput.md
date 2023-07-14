# AWS::MediaConnect::BridgeOutput<a name="aws-resource-mediaconnect-bridgeoutput"></a>

Adds outputs to an existing bridge\.

## Syntax<a name="aws-resource-mediaconnect-bridgeoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediaconnect-bridgeoutput-syntax.json"></a>

```
{
  "Type" : "AWS::MediaConnect::BridgeOutput",
  "Properties" : {
      "[BridgeArn](#cfn-mediaconnect-bridgeoutput-bridgearn)" : String,
      "[Name](#cfn-mediaconnect-bridgeoutput-name)" : String,
      "[NetworkOutput](#cfn-mediaconnect-bridgeoutput-networkoutput)" : BridgeNetworkOutput
    }
}
```

### YAML<a name="aws-resource-mediaconnect-bridgeoutput-syntax.yaml"></a>

```
Type: AWS::MediaConnect::BridgeOutput
Properties: 
  [BridgeArn](#cfn-mediaconnect-bridgeoutput-bridgearn): String
  [Name](#cfn-mediaconnect-bridgeoutput-name): String
  [NetworkOutput](#cfn-mediaconnect-bridgeoutput-networkoutput): 
    BridgeNetworkOutput
```

## Properties<a name="aws-resource-mediaconnect-bridgeoutput-properties"></a>

`BridgeArn`  <a name="cfn-mediaconnect-bridgeoutput-bridgearn"></a>
The ARN of the bridge that you want to describe\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-mediaconnect-bridgeoutput-name"></a>
The network output name\. This name is used to reference the output and must be unique among outputs in this bridge\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkOutput`  <a name="cfn-mediaconnect-bridgeoutput-networkoutput"></a>
Add a network output to an existing bridge\.  
*Required*: Yes  
*Type*: [BridgeNetworkOutput](aws-properties-mediaconnect-bridgeoutput-bridgenetworkoutput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediaconnect-bridgeoutput-return-values"></a>

### Ref<a name="aws-resource-mediaconnect-bridgeoutput-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the bridge ARN and the bridge name\. For example:

`{ "Ref": "arn:aws:mediaconnect:us-east-1:111122223333:bridge:1-23aBC45dEF67hiJ8-12AbC34DE5fG:BasketballArenaIngress|Output:PrimaryOutput1" }`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.