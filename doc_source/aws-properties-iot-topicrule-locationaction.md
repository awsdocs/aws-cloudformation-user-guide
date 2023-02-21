# AWS::IoT::TopicRule LocationAction<a name="aws-properties-iot-topicrule-locationaction"></a>

Describes an action to send device location updates from an MQTT message to an Amazon Location tracker resource\.

## Syntax<a name="aws-properties-iot-topicrule-locationaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-locationaction-syntax.json"></a>

```
{
  "[DeviceId](#cfn-iot-topicrule-locationaction-deviceid)" : String,
  "[Latitude](#cfn-iot-topicrule-locationaction-latitude)" : String,
  "[Longitude](#cfn-iot-topicrule-locationaction-longitude)" : String,
  "[RoleArn](#cfn-iot-topicrule-locationaction-rolearn)" : String,
  "[Timestamp](#cfn-iot-topicrule-locationaction-timestamp)" : Timestamp,
  "[TrackerName](#cfn-iot-topicrule-locationaction-trackername)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-locationaction-syntax.yaml"></a>

```
  [DeviceId](#cfn-iot-topicrule-locationaction-deviceid): String
  [Latitude](#cfn-iot-topicrule-locationaction-latitude): String
  [Longitude](#cfn-iot-topicrule-locationaction-longitude): String
  [RoleArn](#cfn-iot-topicrule-locationaction-rolearn): String
  [Timestamp](#cfn-iot-topicrule-locationaction-timestamp): 
    Timestamp
  [TrackerName](#cfn-iot-topicrule-locationaction-trackername): String
```

## Properties<a name="aws-properties-iot-topicrule-locationaction-properties"></a>

`DeviceId`  <a name="cfn-iot-topicrule-locationaction-deviceid"></a>
The unique ID of the device providing the location data\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Latitude`  <a name="cfn-iot-topicrule-locationaction-latitude"></a>
A string that evaluates to a double value that represents the latitude of the device's location\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Longitude`  <a name="cfn-iot-topicrule-locationaction-longitude"></a>
A string that evaluates to a double value that represents the longitude of the device's location\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-locationaction-rolearn"></a>
The IAM role that grants permission to write to the Amazon Location resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timestamp`  <a name="cfn-iot-topicrule-locationaction-timestamp"></a>
The time that the location data was sampled\. The default value is the time the MQTT message was processed\.  
*Required*: No  
*Type*: [Timestamp](aws-properties-iot-topicrule-timestamp.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrackerName`  <a name="cfn-iot-topicrule-locationaction-trackername"></a>
The name of the tracker resource in Amazon Location in which the location is updated\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)