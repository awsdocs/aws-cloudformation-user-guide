# AWS::IoTAnalytics::Channel<a name="aws-resource-iotanalytics-channel"></a>

The `AWS::IoTAnalytics::Channel` resource collects data from an MQTT topic and archives the raw, unprocessed messages before publishing the data to a pipeline\. For more information, see [ How to Use AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide*\. 

## Syntax<a name="aws-resource-iotanalytics-channel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotanalytics-channel-syntax.json"></a>

```
{
  "Type" : "AWS::IoTAnalytics::Channel",
  "Properties" : {
    "[ChannelName](#cfn-iotanalytics-channel-channelname)" : String,
    "[RetentionPeriod](#cfn-iotanalytics-channel-retentionperiod)" : [*RetentionPeriod*](aws-properties-iotanalytics-channel-retentionperiod.md),
    "[Tags](#cfn-iotanalytics-channel-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ]
  }
}
```

### YAML<a name="aws-resource-iotanalytics-channel-syntax.yaml"></a>

```
Type: "AWS::IoTAnalytics::Channel"
Properties:
  [ChannelName](#cfn-iotanalytics-channel-channelname): String
  [RetentionPeriod](#cfn-iotanalytics-channel-retentionperiod): 
    [*RetentionPeriod*](aws-properties-iotanalytics-channel-retentionperiod.md)
  [Tags](#cfn-iotanalytics-channel-tags): 
    - [*Tag*](aws-properties-resource-tags.md)
```

## Properties<a name="aws-resource-iotanalytics-channel-properties"></a>

`ChannelName`  <a name="cfn-iotanalytics-channel-channelname"></a>
The name of the channel\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`RetentionPeriod`  <a name="cfn-iotanalytics-channel-retentionperiod"></a>
How long, in days, message data is kept for the channel\.  
 *Required*: No  
 *Type*: [RetentionPeriod](aws-properties-iotanalytics-channel-retentionperiod.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-iotanalytics-channel-tags"></a>
Metadata which can be used to manage the channel\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Examples<a name="aws-resource-iotanalytics-channel-examples"></a>

### Simple Channel<a name="aws-resource-iotanalytics-channel-example1"></a>

The following example creates a simple channel\.

#### JSON<a name="aws-resource-iotanalytics-channel-example1.json"></a>

```
{
    "Description": "Create a simple Channel",
    "Resources": {
        "Channel": {
            "Type": "AWS::IoTAnalytics::Channel",
            "Properties": {
                "ChannelName": "SimpleChannel"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-iotanalytics-channel-example1.yaml"></a>

```
---
Description: "Create a simple Channel"
Resources:
  Channel:
    Type: "AWS::IoTAnalytics::Channel"
    Properties:
      ChannelName: "SimpleChannel"
```

### Complex Channel<a name="aws-resource-iotanalytics-channel-example2"></a>

The following example creates a complex channel\.

#### JSON<a name="aws-resource-iotanalytics-channel-example2.json"></a>

```
{
    "Description": "Create a complex channel",
    "Resources": {
        "Channel": {
            "Type": "AWS::IoTAnalytics::Channel",
            "Properties": {
                "ChannelName": "ComplexChannel",
                "RetentionPeriod": {
                    "Unlimited": false,
                    "NumberOfDays": 10
                },
                "Tags": [
                    {
                        "Key": "keyname1",
                        "Value": "value1"
                    },
                    {
                        "Key": "keyname2",
                        "Value": "value2"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-iotanalytics-channel-example2.yaml"></a>

```
---
Description: "Create a complex channel"
Resources:
  Channel:
    Type: "AWS::IoTAnalytics::Channel"
    Properties:
      ChannelName: "ComplexChannel"
      RetentionPeriod:
        Unlimited: false
        NumberOfDays: 10
      Tags:
        -
          Key: "keyname1"
          Value: "value1"
        -
          Key: "keyname2"
          Value: "value2"
```

## See Also<a name="aws-resource-iotanalytics-channel-seealso"></a>
+ [ How to User AWS IoT Analytics](https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html#aws-iot-analytics-how) in the *AWS IoT Analytics User Guide*