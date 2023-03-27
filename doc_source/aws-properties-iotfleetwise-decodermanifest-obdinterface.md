# AWS::IoTFleetWise::DecoderManifest ObdInterface<a name="aws-properties-iotfleetwise-decodermanifest-obdinterface"></a>

A network interface that specifies the On\-board diagnostic \(OBD\) II network protocol\.

## Syntax<a name="aws-properties-iotfleetwise-decodermanifest-obdinterface-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-decodermanifest-obdinterface-syntax.json"></a>

```
{
  "[DtcRequestIntervalSeconds](#cfn-iotfleetwise-decodermanifest-obdinterface-dtcrequestintervalseconds)" : String,
  "[HasTransmissionEcu](#cfn-iotfleetwise-decodermanifest-obdinterface-hastransmissionecu)" : String,
  "[Name](#cfn-iotfleetwise-decodermanifest-obdinterface-name)" : String,
  "[ObdStandard](#cfn-iotfleetwise-decodermanifest-obdinterface-obdstandard)" : String,
  "[PidRequestIntervalSeconds](#cfn-iotfleetwise-decodermanifest-obdinterface-pidrequestintervalseconds)" : String,
  "[RequestMessageId](#cfn-iotfleetwise-decodermanifest-obdinterface-requestmessageid)" : String,
  "[UseExtendedIds](#cfn-iotfleetwise-decodermanifest-obdinterface-useextendedids)" : String
}
```

### YAML<a name="aws-properties-iotfleetwise-decodermanifest-obdinterface-syntax.yaml"></a>

```
  [DtcRequestIntervalSeconds](#cfn-iotfleetwise-decodermanifest-obdinterface-dtcrequestintervalseconds): String
  [HasTransmissionEcu](#cfn-iotfleetwise-decodermanifest-obdinterface-hastransmissionecu): String
  [Name](#cfn-iotfleetwise-decodermanifest-obdinterface-name): String
  [ObdStandard](#cfn-iotfleetwise-decodermanifest-obdinterface-obdstandard): String
  [PidRequestIntervalSeconds](#cfn-iotfleetwise-decodermanifest-obdinterface-pidrequestintervalseconds): String
  [RequestMessageId](#cfn-iotfleetwise-decodermanifest-obdinterface-requestmessageid): String
  [UseExtendedIds](#cfn-iotfleetwise-decodermanifest-obdinterface-useextendedids): String
```

## Properties<a name="aws-properties-iotfleetwise-decodermanifest-obdinterface-properties"></a>

`DtcRequestIntervalSeconds`  <a name="cfn-iotfleetwise-decodermanifest-obdinterface-dtcrequestintervalseconds"></a>
The maximum number message requests per diagnostic trouble code per second\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HasTransmissionEcu`  <a name="cfn-iotfleetwise-decodermanifest-obdinterface-hastransmissionecu"></a>
Whether the vehicle has a transmission control module \(TCM\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotfleetwise-decodermanifest-obdinterface-name"></a>
The name of the interface\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObdStandard`  <a name="cfn-iotfleetwise-decodermanifest-obdinterface-obdstandard"></a>
The standard OBD II PID\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PidRequestIntervalSeconds`  <a name="cfn-iotfleetwise-decodermanifest-obdinterface-pidrequestintervalseconds"></a>
The maximum number message requests per second\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestMessageId`  <a name="cfn-iotfleetwise-decodermanifest-obdinterface-requestmessageid"></a>
The ID of the message requesting vehicle data\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseExtendedIds`  <a name="cfn-iotfleetwise-decodermanifest-obdinterface-useextendedids"></a>
Whether to use extended IDs in the message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)