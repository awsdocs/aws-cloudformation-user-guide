# AWS::NetworkManager::CoreNetwork CoreNetworkSegment<a name="aws-properties-networkmanager-corenetwork-corenetworksegment"></a>

Describes a core network segment, which are dedicated routes\. Only attachments within this segment can communicate with each other\.

## Syntax<a name="aws-properties-networkmanager-corenetwork-corenetworksegment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkmanager-corenetwork-corenetworksegment-syntax.json"></a>

```
{
  "[EdgeLocations](#cfn-networkmanager-corenetwork-corenetworksegment-edgelocations)" : [ String, ... ],
  "[Name](#cfn-networkmanager-corenetwork-corenetworksegment-name)" : String,
  "[SharedSegments](#cfn-networkmanager-corenetwork-corenetworksegment-sharedsegments)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-networkmanager-corenetwork-corenetworksegment-syntax.yaml"></a>

```
  [EdgeLocations](#cfn-networkmanager-corenetwork-corenetworksegment-edgelocations): 
    - String
  [Name](#cfn-networkmanager-corenetwork-corenetworksegment-name): String
  [SharedSegments](#cfn-networkmanager-corenetwork-corenetworksegment-sharedsegments): 
    - String
```

## Properties<a name="aws-properties-networkmanager-corenetwork-corenetworksegment-properties"></a>

`EdgeLocations`  <a name="cfn-networkmanager-corenetwork-corenetworksegment-edgelocations"></a>
The Regions where the edges are located\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-networkmanager-corenetwork-corenetworksegment-name"></a>
The name of a core network segment\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\s\S]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SharedSegments`  <a name="cfn-networkmanager-corenetwork-corenetworksegment-sharedsegments"></a>
The shared segments of a core network\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)