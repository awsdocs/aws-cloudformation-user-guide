# AWS::IoTSiteWise::AssetModel AssetModelProperty<a name="aws-properties-iotsitewise-assetmodel-assetmodelproperty"></a>

Contains information about an asset model property\.

## Syntax<a name="aws-properties-iotsitewise-assetmodel-assetmodelproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-assetmodel-assetmodelproperty-syntax.json"></a>

```
{
  "[DataType](#cfn-iotsitewise-assetmodel-assetmodelproperty-datatype)" : String,
  "[LogicalId](#cfn-iotsitewise-assetmodel-assetmodelproperty-logicalid)" : String,
  "[Name](#cfn-iotsitewise-assetmodel-assetmodelproperty-name)" : String,
  "[Type](#cfn-iotsitewise-assetmodel-assetmodelproperty-type)" : PropertyType,
  "[Unit](#cfn-iotsitewise-assetmodel-assetmodelproperty-unit)" : String
}
```

### YAML<a name="aws-properties-iotsitewise-assetmodel-assetmodelproperty-syntax.yaml"></a>

```
  [DataType](#cfn-iotsitewise-assetmodel-assetmodelproperty-datatype): String
  [LogicalId](#cfn-iotsitewise-assetmodel-assetmodelproperty-logicalid): String
  [Name](#cfn-iotsitewise-assetmodel-assetmodelproperty-name): String
  [Type](#cfn-iotsitewise-assetmodel-assetmodelproperty-type): 
    PropertyType
  [Unit](#cfn-iotsitewise-assetmodel-assetmodelproperty-unit): String
```

## Properties<a name="aws-properties-iotsitewise-assetmodel-assetmodelproperty-properties"></a>

`DataType`  <a name="cfn-iotsitewise-assetmodel-assetmodelproperty-datatype"></a>
The data type of the asset model property, which can be one of `BOOLEAN`, `INTEGER`, `DOUBLE`, or `STRING`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogicalId`  <a name="cfn-iotsitewise-assetmodel-assetmodelproperty-logicalid"></a>
The `LogicalID` of the asset model property\.  
The maximum length is 256 characters, with the pattern `[^\\u0000-\\u001F\\u007F]+`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotsitewise-assetmodel-assetmodelproperty-name"></a>
The name of the asset model property\.  
The maximum length is 256 characters with the pattern `[^\u0000-\u001F\u007F]+`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-iotsitewise-assetmodel-assetmodelproperty-type"></a>
Contains a property type, which can be one of `attribute`, `measurement`, `metric`, or `transform`\.  
*Required*: Yes  
*Type*: [PropertyType](aws-properties-iotsitewise-assetmodel-propertytype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-iotsitewise-assetmodel-assetmodelproperty-unit"></a>
The unit of the asset model property, such as `Newtons` or `RPM`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)