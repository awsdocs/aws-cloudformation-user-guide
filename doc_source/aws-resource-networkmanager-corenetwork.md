# AWS::NetworkManager::CoreNetwork<a name="aws-resource-networkmanager-corenetwork"></a>

Describes a core network\.

## Syntax<a name="aws-resource-networkmanager-corenetwork-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-corenetwork-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::CoreNetwork",
  "Properties" : {
      "[Description](#cfn-networkmanager-corenetwork-description)" : String,
      "[GlobalNetworkId](#cfn-networkmanager-corenetwork-globalnetworkid)" : String,
      "[PolicyDocument](#cfn-networkmanager-corenetwork-policydocument)" : Json,
      "[Tags](#cfn-networkmanager-corenetwork-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-networkmanager-corenetwork-syntax.yaml"></a>

```
Type: AWS::NetworkManager::CoreNetwork
Properties: 
  [Description](#cfn-networkmanager-corenetwork-description): String
  [GlobalNetworkId](#cfn-networkmanager-corenetwork-globalnetworkid): String
  [PolicyDocument](#cfn-networkmanager-corenetwork-policydocument): Json
  [Tags](#cfn-networkmanager-corenetwork-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-networkmanager-corenetwork-properties"></a>

`Description`  <a name="cfn-networkmanager-corenetwork-description"></a>
The description of a core network\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\s\S]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalNetworkId`  <a name="cfn-networkmanager-corenetwork-globalnetworkid"></a>
The ID of the global network that your core network is a part of\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `50`  
*Pattern*: `[\s\S]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PolicyDocument`  <a name="cfn-networkmanager-corenetwork-policydocument"></a>
Describes a core network policy\. For more information, see [Core network policies](https://docs.aws.amazon.com/vpc/latest/cloudwan/cloudwan-policy-changesets.html)\.  
If you update the policy document, CloudFormation will apply the core network change set generated from the updated policy document, and then set it as the LIVE policy\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-networkmanager-corenetwork-tags"></a>
The list of key\-value tags associated with a core network\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-networkmanager-corenetwork-return-values"></a>

### Ref<a name="aws-resource-networkmanager-corenetwork-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the core network\. For example, `{ "Ref: "core-network-060ea2740fe60fd38" }`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-networkmanager-corenetwork-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-networkmanager-corenetwork-return-values-fn--getatt-fn--getatt"></a>

`CoreNetworkArn`  <a name="CoreNetworkArn-fn::getatt"></a>
The ARN of the core network\.

`CoreNetworkId`  <a name="CoreNetworkId-fn::getatt"></a>
The ID of the core network\.

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp when the core network was created\.

`Edges`  <a name="Edges-fn::getatt"></a>
The edges\.

`OwnerAccount`  <a name="OwnerAccount-fn::getatt"></a>
Property description not available\.

`Segments`  <a name="Segments-fn::getatt"></a>
The segments\.

`State`  <a name="State-fn::getatt"></a>
The current state of the core network\. These states are: `CREATING` \| `UPDATING` \| `AVAILABLE` \| `DELETING`\. 