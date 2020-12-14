# AWS::IoTSiteWise::AssetModel AssetModelHierarchy<a name="aws-properties-iotsitewise-assetmodel-assetmodelhierarchy"></a>

Describes an asset hierarchy that contains a hierarchy's name, `LogicalID`, and child asset model ID that specifies the type of asset that can be in this hierarchy\.

## Syntax<a name="aws-properties-iotsitewise-assetmodel-assetmodelhierarchy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-assetmodel-assetmodelhierarchy-syntax.json"></a>

```
{
  "[ChildAssetModelId](#cfn-iotsitewise-assetmodel-assetmodelhierarchy-childassetmodelid)" : String,
  "[LogicalId](#cfn-iotsitewise-assetmodel-assetmodelhierarchy-logicalid)" : String,
  "[Name](#cfn-iotsitewise-assetmodel-assetmodelhierarchy-name)" : String
}
```

### YAML<a name="aws-properties-iotsitewise-assetmodel-assetmodelhierarchy-syntax.yaml"></a>

```
  [ChildAssetModelId](#cfn-iotsitewise-assetmodel-assetmodelhierarchy-childassetmodelid): String
  [LogicalId](#cfn-iotsitewise-assetmodel-assetmodelhierarchy-logicalid): String
  [Name](#cfn-iotsitewise-assetmodel-assetmodelhierarchy-name): String
```

## Properties<a name="aws-properties-iotsitewise-assetmodel-assetmodelhierarchy-properties"></a>

`ChildAssetModelId`  <a name="cfn-iotsitewise-assetmodel-assetmodelhierarchy-childassetmodelid"></a>
The Id of the asset model\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogicalId`  <a name="cfn-iotsitewise-assetmodel-assetmodelhierarchy-logicalid"></a>
The `LogicalID` of the asset model hierarchy\. This ID is a `hierarchyLogicalId`\.  
The maximum length is 256 characters, with the pattern `[^\u0000-\u001F\u007F]+`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotsitewise-assetmodel-assetmodelhierarchy-name"></a>
The name of the asset model hierarchy\.   
The maximum length is 256 characters with the pattern `[^\u0000-\u001F\u007F]+`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)