# AWS::IoTSiteWise::AssetModel<a name="aws-resource-iotsitewise-assetmodel"></a>

Creates an asset model from specified property and hierarchy definitions\. You create assets from asset models\. With asset models, you can easily create assets of the same type that have standardized definitions\. Each asset created from a model inherits the asset model's property and hierarchy definitions\. For more information, see [Defining asset models](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/define-models.html) in the *AWS IoT SiteWise User Guide*\.

## Syntax<a name="aws-resource-iotsitewise-assetmodel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotsitewise-assetmodel-syntax.json"></a>

```
{
  "Type" : "AWS::IoTSiteWise::AssetModel",
  "Properties" : {
      "[AssetModelDescription](#cfn-iotsitewise-assetmodel-assetmodeldescription)" : String,
      "[AssetModelHierarchies](#cfn-iotsitewise-assetmodel-assetmodelhierarchies)" : [ AssetModelHierarchy, ... ],
      "[AssetModelName](#cfn-iotsitewise-assetmodel-assetmodelname)" : String,
      "[AssetModelProperties](#cfn-iotsitewise-assetmodel-assetmodelproperties)" : [ AssetModelProperty, ... ],
      "[Tags](#cfn-iotsitewise-assetmodel-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotsitewise-assetmodel-syntax.yaml"></a>

```
Type: AWS::IoTSiteWise::AssetModel
Properties: 
  [AssetModelDescription](#cfn-iotsitewise-assetmodel-assetmodeldescription): String
  [AssetModelHierarchies](#cfn-iotsitewise-assetmodel-assetmodelhierarchies): 
    - AssetModelHierarchy
  [AssetModelName](#cfn-iotsitewise-assetmodel-assetmodelname): String
  [AssetModelProperties](#cfn-iotsitewise-assetmodel-assetmodelproperties): 
    - AssetModelProperty
  [Tags](#cfn-iotsitewise-assetmodel-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotsitewise-assetmodel-properties"></a>

`AssetModelDescription`  <a name="cfn-iotsitewise-assetmodel-assetmodeldescription"></a>
A description for the asset model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AssetModelHierarchies`  <a name="cfn-iotsitewise-assetmodel-assetmodelhierarchies"></a>
The hierarchy definitions of the asset model\. Each hierarchy specifies an asset model whose assets can be children of any other assets created from this asset model\. For more information, see [Defining relationships between assets](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/asset-hierarchies.html) in the *AWS IoT SiteWise User Guide*\.  
You can specify up to 10 hierarchies per asset model\. For more information, see [Quotas](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/quotas.html) in the *AWS IoT SiteWise User Guide*\.  
*Required*: No  
*Type*: List of [AssetModelHierarchy](aws-properties-iotsitewise-assetmodel-assetmodelhierarchy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AssetModelName`  <a name="cfn-iotsitewise-assetmodel-assetmodelname"></a>
A unique, friendly name for the asset model\.  
The maximum length is 256 characters with the pattern `[^\u0000-\u001F\u007F]+`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AssetModelProperties`  <a name="cfn-iotsitewise-assetmodel-assetmodelproperties"></a>
The property definitions of the asset model\. For more information, see [Defining data properties](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/asset-properties.html) in the *AWS IoT SiteWise User Guide*\.  
You can specify up to 200 properties per asset model\. For more information, see [Quotas](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/quotas.html) in the *AWS IoT SiteWise User Guide*\.  
*Required*: No  
*Type*: List of [AssetModelProperty](aws-properties-iotsitewise-assetmodel-assetmodelproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotsitewise-assetmodel-tags"></a>
A list of key\-value pairs that contain metadata for the asset\. For more information, see [Tagging your AWS IoT SiteWise resources](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/tag-resources.html) in the *AWS IoT SiteWise User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotsitewise-assetmodel-return-values"></a>

### Ref<a name="aws-resource-iotsitewise-assetmodel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `AssetModelId`\.

### Fn::GetAtt<a name="aws-resource-iotsitewise-assetmodel-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iotsitewise-assetmodel-return-values-fn--getatt-fn--getatt"></a>

`AssetModelId`  <a name="AssetModelId-fn::getatt"></a>
The ID of the asset model\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.