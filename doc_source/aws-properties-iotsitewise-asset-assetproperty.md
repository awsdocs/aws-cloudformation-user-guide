# AWS::IoTSiteWise::Asset AssetProperty<a name="aws-properties-iotsitewise-asset-assetproperty"></a>

Contains asset property information\.

## Syntax<a name="aws-properties-iotsitewise-asset-assetproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-asset-assetproperty-syntax.json"></a>

```
{
  "[Alias](#cfn-iotsitewise-asset-assetproperty-alias)" : String,
  "[LogicalId](#cfn-iotsitewise-asset-assetproperty-logicalid)" : String,
  "[NotificationState](#cfn-iotsitewise-asset-assetproperty-notificationstate)" : String
}
```

### YAML<a name="aws-properties-iotsitewise-asset-assetproperty-syntax.yaml"></a>

```
  [Alias](#cfn-iotsitewise-asset-assetproperty-alias): String
  [LogicalId](#cfn-iotsitewise-asset-assetproperty-logicalid): String
  [NotificationState](#cfn-iotsitewise-asset-assetproperty-notificationstate): String
```

## Properties<a name="aws-properties-iotsitewise-asset-assetproperty-properties"></a>

`Alias`  <a name="cfn-iotsitewise-asset-assetproperty-alias"></a>
The property alias that identifies the property, such as an OPC\-UA server data stream path \(for example, `/company/windfarm/3/turbine/7/temperature`\)\. For more information, see [Mapping industrial data streams to asset properties](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/connect-data-streams.html) in the *AWS IoT SiteWise User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogicalId`  <a name="cfn-iotsitewise-asset-assetproperty-logicalid"></a>
The `LogicalID` of the asset property\.  
The maximum length is 256 characters, with the pattern `[^\u0000-\u001F\u007F]+`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationState`  <a name="cfn-iotsitewise-asset-assetproperty-notificationstate"></a>
The MQTT notification state \(enabled or disabled\) for this asset property\. When the notification state is enabled, AWS IoT SiteWise publishes property value updates to a unique MQTT topic\. For more information, see [Interacting with other services](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/interact-with-other-services.html) in the *AWS IoT SiteWise User Guide*\.  
If you omit this parameter, the notification state is set to `DISABLED`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)