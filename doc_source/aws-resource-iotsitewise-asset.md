# AWS::IoTSiteWise::Asset<a name="aws-resource-iotsitewise-asset"></a>

Creates an asset from an existing asset model\. For more information, see [Creating assets](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/create-assets.html) in the *AWS IoT SiteWise User Guide*\.

## Syntax<a name="aws-resource-iotsitewise-asset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotsitewise-asset-syntax.json"></a>

```
{
  "Type" : "AWS::IoTSiteWise::Asset",
  "Properties" : {
      "[AssetHierarchies](#cfn-iotsitewise-asset-assethierarchies)" : [ AssetHierarchy, ... ],
      "[AssetModelId](#cfn-iotsitewise-asset-assetmodelid)" : String,
      "[AssetName](#cfn-iotsitewise-asset-assetname)" : String,
      "[AssetProperties](#cfn-iotsitewise-asset-assetproperties)" : [ AssetProperty, ... ],
      "[Tags](#cfn-iotsitewise-asset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotsitewise-asset-syntax.yaml"></a>

```
Type: AWS::IoTSiteWise::Asset
Properties: 
  [AssetHierarchies](#cfn-iotsitewise-asset-assethierarchies): 
    - AssetHierarchy
  [AssetModelId](#cfn-iotsitewise-asset-assetmodelid): String
  [AssetName](#cfn-iotsitewise-asset-assetname): String
  [AssetProperties](#cfn-iotsitewise-asset-assetproperties): 
    - AssetProperty
  [Tags](#cfn-iotsitewise-asset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotsitewise-asset-properties"></a>

`AssetHierarchies`  <a name="cfn-iotsitewise-asset-assethierarchies"></a>
A list of asset hierarchies that each contain a `hierarchyLogicalId`\. A hierarchy specifies allowed parent/child asset relationships\.  
*Required*: No  
*Type*: List of [AssetHierarchy](aws-properties-iotsitewise-asset-assethierarchy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AssetModelId`  <a name="cfn-iotsitewise-asset-assetmodelid"></a>
The ID of the asset model from which to create the asset\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AssetName`  <a name="cfn-iotsitewise-asset-assetname"></a>
A unique, friendly name for the asset\.  
The maximum length is 256 characters with the pattern `[^\u0000-\u001F\u007F]+`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AssetProperties`  <a name="cfn-iotsitewise-asset-assetproperties"></a>
The list of asset properties for the asset\.  
This object doesn't include properties that you define in composite models\. You can find composite model properties in the `assetCompositeModels` object\.  
*Required*: No  
*Type*: List of [AssetProperty](aws-properties-iotsitewise-asset-assetproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotsitewise-asset-tags"></a>
A list of key\-value pairs that contain metadata for the asset\. For more information, see [Tagging your AWS IoT SiteWise resources](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/tag-resources.html) in the *AWS IoT SiteWise User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotsitewise-asset-return-values"></a>

### Ref<a name="aws-resource-iotsitewise-asset-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `AssetId`\.

### Fn::GetAtt<a name="aws-resource-iotsitewise-asset-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iotsitewise-asset-return-values-fn--getatt-fn--getatt"></a>

`AssetId`  <a name="AssetId-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.