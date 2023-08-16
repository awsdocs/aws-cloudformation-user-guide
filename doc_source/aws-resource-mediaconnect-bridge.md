# AWS::MediaConnect::Bridge<a name="aws-resource-mediaconnect-bridge"></a>

The AWS::MediaConnect::Bridge resource defines a connection between your data center’s gateway instances and the cloud\. For each bridge, you specify the type of bridge, transport protocol to use, and details for any outputs and failover\.

## Syntax<a name="aws-resource-mediaconnect-bridge-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediaconnect-bridge-syntax.json"></a>

```
{
  "Type" : "AWS::MediaConnect::Bridge",
  "Properties" : {
      "[EgressGatewayBridge](#cfn-mediaconnect-bridge-egressgatewaybridge)" : EgressGatewayBridge,
      "[IngressGatewayBridge](#cfn-mediaconnect-bridge-ingressgatewaybridge)" : IngressGatewayBridge,
      "[Name](#cfn-mediaconnect-bridge-name)" : String,
      "[Outputs](#cfn-mediaconnect-bridge-outputs)" : [ BridgeOutput, ... ],
      "[PlacementArn](#cfn-mediaconnect-bridge-placementarn)" : String,
      "[SourceFailoverConfig](#cfn-mediaconnect-bridge-sourcefailoverconfig)" : FailoverConfig,
      "[Sources](#cfn-mediaconnect-bridge-sources)" : [ BridgeSource, ... ]
    }
}
```

### YAML<a name="aws-resource-mediaconnect-bridge-syntax.yaml"></a>

```
Type: AWS::MediaConnect::Bridge
Properties: 
  [EgressGatewayBridge](#cfn-mediaconnect-bridge-egressgatewaybridge): 
    EgressGatewayBridge
  [IngressGatewayBridge](#cfn-mediaconnect-bridge-ingressgatewaybridge): 
    IngressGatewayBridge
  [Name](#cfn-mediaconnect-bridge-name): String
  [Outputs](#cfn-mediaconnect-bridge-outputs): 
    - BridgeOutput
  [PlacementArn](#cfn-mediaconnect-bridge-placementarn): String
  [SourceFailoverConfig](#cfn-mediaconnect-bridge-sourcefailoverconfig): 
    FailoverConfig
  [Sources](#cfn-mediaconnect-bridge-sources): 
    - BridgeSource
```

## Properties<a name="aws-resource-mediaconnect-bridge-properties"></a>

`EgressGatewayBridge`  <a name="cfn-mediaconnect-bridge-egressgatewaybridge"></a>
Create a bridge with the egress bridge type\. An egress bridge is a cloud\-to\-ground bridge\. The content comes from an existing MediaConnect flow and is delivered to your premises\.  
*Required*: No  
*Type*: [EgressGatewayBridge](aws-properties-mediaconnect-bridge-egressgatewaybridge.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IngressGatewayBridge`  <a name="cfn-mediaconnect-bridge-ingressgatewaybridge"></a>
Create a bridge with the ingress bridge type\. An ingress bridge is a ground\-to\-cloud bridge\. The content originates at your premises and is delivered to the cloud\.  
*Required*: No  
*Type*: [IngressGatewayBridge](aws-properties-mediaconnect-bridge-ingressgatewaybridge.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mediaconnect-bridge-name"></a>
The network output name\. This name is used to reference the output and must be unique among outputs in this bridge\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Outputs`  <a name="cfn-mediaconnect-bridge-outputs"></a>
The outputs that you want to add to this bridge\.  
*Required*: No  
*Type*: List of [BridgeOutput](aws-properties-mediaconnect-bridge-bridgeoutput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlacementArn`  <a name="cfn-mediaconnect-bridge-placementarn"></a>
The bridge placement Amazon Resource Number \(ARN\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFailoverConfig`  <a name="cfn-mediaconnect-bridge-sourcefailoverconfig"></a>
The settings for source failover\.  
*Required*: No  
*Type*: [FailoverConfig](aws-properties-mediaconnect-bridge-failoverconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sources`  <a name="cfn-mediaconnect-bridge-sources"></a>
The sources that you want to add to this bridge\.  
*Required*: Yes  
*Type*: List of [BridgeSource](aws-properties-mediaconnect-bridge-bridgesource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediaconnect-bridge-return-values"></a>

### Ref<a name="aws-resource-mediaconnect-bridge-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the bridge ARN\. For example:

`{ "Ref": "arn:aws:mediaconnect:us-east-1:111122223333:bridge:1-23aBC45dEF67hiJ8-12AbC34DE5fG:BasketballArenaIngress" }`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-mediaconnect-bridge-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-mediaconnect-bridge-return-values-fn--getatt-fn--getatt"></a>

`BridgeArn`  <a name="BridgeArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the bridge\.

`BridgeState`  <a name="BridgeState-fn::getatt"></a>
The current status of the bridge\. Possible values are: ACTIVE or STANDBY\. 