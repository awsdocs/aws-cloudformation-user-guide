# AWS::IoTSiteWise::Asset AssetHierarchy<a name="aws-properties-iotsitewise-asset-assethierarchy"></a>

Describes an asset hierarchy that contains a `childAssetId` and `hierarchyLogicalId`\.

## Syntax<a name="aws-properties-iotsitewise-asset-assethierarchy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-asset-assethierarchy-syntax.json"></a>

```
{
  "[ChildAssetId](#cfn-iotsitewise-asset-assethierarchy-childassetid)" : String,
  "[LogicalId](#cfn-iotsitewise-asset-assethierarchy-logicalid)" : String
}
```

### YAML<a name="aws-properties-iotsitewise-asset-assethierarchy-syntax.yaml"></a>

```
  [ChildAssetId](#cfn-iotsitewise-asset-assethierarchy-childassetid): String
  [LogicalId](#cfn-iotsitewise-asset-assethierarchy-logicalid): String
```

## Properties<a name="aws-properties-iotsitewise-asset-assethierarchy-properties"></a>

`ChildAssetId`  <a name="cfn-iotsitewise-asset-assethierarchy-childassetid"></a>
The Id of the child asset\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogicalId`  <a name="cfn-iotsitewise-asset-assethierarchy-logicalid"></a>
The `LogicalID` of the hierarchy\. This ID is a `hierarchyLogicalId`\.  
The maximum length is 256 characters, with the pattern `[^\u0000-\u001F\u007F]+`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)