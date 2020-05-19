# AWS::IoTEvents::DetectorModel IotSiteWise<a name="aws-properties-iotevents-detectormodel-iotsitewise"></a>

Sends information about the detector model instance and the event that triggered the action to a specified asset property in AWS IoT SiteWise\.

**Important**  
You must specify either `propertyAlias` or both `assetId` and `propertyId` to identify the target asset property in AWS IoT SiteWise\.

For parameters that are string data type, you can specify the following options: 
+ Use a string\. For example, the `propertyAlias` value can be `'/company/windfarm/3/turbine/7/temperature'`\.
+ Use an expression\. For example, the `propertyAlias` value can be `'company/windfarm/${$input.TemperatureInput.sensorData.windfarmID}/turbine/${$input.TemperatureInput.sensorData.turbineID}/temperature'`\.

  For more information, see [Expressions](https://docs.aws.amazon.com/iotevents/latest/developerguide/iotevents-expressions.html) in the *AWS IoT Events Developer Guide*\.

## Syntax<a name="aws-properties-iotevents-detectormodel-iotsitewise-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-iotsitewise-syntax.json"></a>

```
{
  "[AssetId](#cfn-iotevents-detectormodel-iotsitewise-assetid)" : String,
  "[EntryId](#cfn-iotevents-detectormodel-iotsitewise-entryid)" : String,
  "[PropertyAlias](#cfn-iotevents-detectormodel-iotsitewise-propertyalias)" : String,
  "[PropertyId](#cfn-iotevents-detectormodel-iotsitewise-propertyid)" : String,
  "[PropertyValue](#cfn-iotevents-detectormodel-iotsitewise-propertyvalue)" : [AssetPropertyValue](aws-properties-iotevents-detectormodel-assetpropertyvalue.md)
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-iotsitewise-syntax.yaml"></a>

```
  [AssetId](#cfn-iotevents-detectormodel-iotsitewise-assetid): String
  [EntryId](#cfn-iotevents-detectormodel-iotsitewise-entryid): String
  [PropertyAlias](#cfn-iotevents-detectormodel-iotsitewise-propertyalias): String
  [PropertyId](#cfn-iotevents-detectormodel-iotsitewise-propertyid): String
  [PropertyValue](#cfn-iotevents-detectormodel-iotsitewise-propertyvalue): 
    [AssetPropertyValue](aws-properties-iotevents-detectormodel-assetpropertyvalue.md)
```

## Properties<a name="aws-properties-iotevents-detectormodel-iotsitewise-properties"></a>

`AssetId`  <a name="cfn-iotevents-detectormodel-iotsitewise-assetid"></a>
The ID of the asset that has the specified property\. You can specify an expression\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntryId`  <a name="cfn-iotevents-detectormodel-iotsitewise-entryid"></a>
A unique identifier for this entry\. You can use the entry ID to track which data entry causes an error in case of failure\. The default is a new unique identifier\. You can also specify an expression\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropertyAlias`  <a name="cfn-iotevents-detectormodel-iotsitewise-propertyalias"></a>
The alias of the asset property\. You can also specify an expression\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropertyId`  <a name="cfn-iotevents-detectormodel-iotsitewise-propertyid"></a>
The ID of the asset property\. You can specify an expression\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropertyValue`  <a name="cfn-iotevents-detectormodel-iotsitewise-propertyvalue"></a>
The value to send to the asset property\. This value contains timestamp, quality, and value \(TQV\) information\.   
*Required*: No  
*Type*: [AssetPropertyValue](aws-properties-iotevents-detectormodel-assetpropertyvalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)