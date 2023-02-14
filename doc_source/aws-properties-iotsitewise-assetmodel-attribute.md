# AWS::IoTSiteWise::AssetModel Attribute<a name="aws-properties-iotsitewise-assetmodel-attribute"></a>

Contains an asset attribute property\. For more information, see [Defining data properties](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/asset-properties.html#attributes) in the *AWS IoT SiteWise User Guide*\.

## Syntax<a name="aws-properties-iotsitewise-assetmodel-attribute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-assetmodel-attribute-syntax.json"></a>

```
{
  "[DefaultValue](#cfn-iotsitewise-assetmodel-attribute-defaultvalue)" : String
}
```

### YAML<a name="aws-properties-iotsitewise-assetmodel-attribute-syntax.yaml"></a>

```
  [DefaultValue](#cfn-iotsitewise-assetmodel-attribute-defaultvalue): String
```

## Properties<a name="aws-properties-iotsitewise-assetmodel-attribute-properties"></a>

`DefaultValue`  <a name="cfn-iotsitewise-assetmodel-attribute-defaultvalue"></a>
The default value of the asset model property attribute\. All assets that you create from the asset model contain this attribute value\. You can update an attribute's value after you create an asset\. For more information, see [Updating attribute values](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/update-attribute-values.html) in the *AWS IoT SiteWise User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)