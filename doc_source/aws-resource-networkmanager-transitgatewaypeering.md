# AWS::NetworkManager::TransitGatewayPeering<a name="aws-resource-networkmanager-transitgatewaypeering"></a>

Creates a transit gateway peering connection\.

## Syntax<a name="aws-resource-networkmanager-transitgatewaypeering-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-transitgatewaypeering-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::TransitGatewayPeering",
  "Properties" : {
      "[CoreNetworkId](#cfn-networkmanager-transitgatewaypeering-corenetworkid)" : String,
      "[Tags](#cfn-networkmanager-transitgatewaypeering-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TransitGatewayArn](#cfn-networkmanager-transitgatewaypeering-transitgatewayarn)" : String
    }
}
```

### YAML<a name="aws-resource-networkmanager-transitgatewaypeering-syntax.yaml"></a>

```
Type: AWS::NetworkManager::TransitGatewayPeering
Properties: 
  [CoreNetworkId](#cfn-networkmanager-transitgatewaypeering-corenetworkid): String
  [Tags](#cfn-networkmanager-transitgatewaypeering-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TransitGatewayArn](#cfn-networkmanager-transitgatewaypeering-transitgatewayarn): String
```

## Properties<a name="aws-resource-networkmanager-transitgatewaypeering-properties"></a>

`CoreNetworkId`  <a name="cfn-networkmanager-transitgatewaypeering-corenetworkid"></a>
The ID of the core network\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-networkmanager-transitgatewaypeering-tags"></a>
The list of key\-value tags associated with the peering\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitGatewayArn`  <a name="cfn-networkmanager-transitgatewaypeering-transitgatewayarn"></a>
The ARN of the transit gateway\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `500`  
*Pattern*: `[\s\S]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-networkmanager-transitgatewaypeering-return-values"></a>

### Ref<a name="aws-resource-networkmanager-transitgatewaypeering-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `peeringId`\. For example: `peering-01234ab1234a12a12`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-networkmanager-transitgatewaypeering-return-values-fn--getatt"></a>

#### <a name="aws-resource-networkmanager-transitgatewaypeering-return-values-fn--getatt-fn--getatt"></a>

`CoreNetworkArn`  <a name="CoreNetworkArn-fn::getatt"></a>
The ARN of the core network\.

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp when the core network peering was created\.

`EdgeLocation`  <a name="EdgeLocation-fn::getatt"></a>
The edge location for the peer\.

`OwnerAccountId`  <a name="OwnerAccountId-fn::getatt"></a>
The ID of the account owner\.

`PeeringId`  <a name="PeeringId-fn::getatt"></a>
The ID of the peering\.

`PeeringType`  <a name="PeeringType-fn::getatt"></a>
The peering type\. This will be `TRANSIT_GATEWAY`\.

`ResourceArn`  <a name="ResourceArn-fn::getatt"></a>
The ARN of the resource peered to a core network\.

`State`  <a name="State-fn::getatt"></a>
The current state of the peer\. This can be `CREATING` \| `FAILED` \| `AVAILABLE` \| `DELETING`\.

`TransitGatewayPeeringAttachmentId`  <a name="TransitGatewayPeeringAttachmentId-fn::getatt"></a>
The ID of the peering attachment\.