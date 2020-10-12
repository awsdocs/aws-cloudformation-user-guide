# AWS::IoT::TopicRule IotSiteWiseAction<a name="aws-properties-iot-topicrule-iotsitewiseaction"></a>

Describes an action to send data from an MQTT message that triggered the rule to AWS IoT SiteWise asset properties\.

## Syntax<a name="aws-properties-iot-topicrule-iotsitewiseaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-iotsitewiseaction-syntax.json"></a>

```
{
  "[PutAssetPropertyValueEntries](#cfn-iot-topicrule-iotsitewiseaction-putassetpropertyvalueentries)" : [ PutAssetPropertyValueEntry, ... ],
  "[RoleArn](#cfn-iot-topicrule-iotsitewiseaction-rolearn)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-iotsitewiseaction-syntax.yaml"></a>

```
  [PutAssetPropertyValueEntries](#cfn-iot-topicrule-iotsitewiseaction-putassetpropertyvalueentries): 
    - PutAssetPropertyValueEntry
  [RoleArn](#cfn-iot-topicrule-iotsitewiseaction-rolearn): String
```

## Properties<a name="aws-properties-iot-topicrule-iotsitewiseaction-properties"></a>

`PutAssetPropertyValueEntries`  <a name="cfn-iot-topicrule-iotsitewiseaction-putassetpropertyvalueentries"></a>
A list of asset property value entries\.  
*Required*: Yes  
*Type*: List of [PutAssetPropertyValueEntry](aws-properties-iot-topicrule-putassetpropertyvalueentry.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-iotsitewiseaction-rolearn"></a>
The ARN of the role that grants AWS IoT permission to send an asset property value to AWS IoTSiteWise\. \(`"Action": "iotsitewise:BatchPutAssetPropertyValue"`\)\. The trust policy can restrict access to specific asset hierarchy paths\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)