# AWS::IoTEvents::DetectorModel Firehose<a name="aws-properties-iotevents-detectormodel-firehose"></a>

Sends information about the detector model instance and the event which triggered the action to a Kinesis Data Firehose delivery stream\.

## Syntax<a name="aws-properties-iotevents-detectormodel-firehose-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-firehose-syntax.json"></a>

```
{
  "[DeliveryStreamName](#cfn-iotevents-detectormodel-firehose-deliverystreamname)" : String,
  "[Separator](#cfn-iotevents-detectormodel-firehose-separator)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-firehose-syntax.yaml"></a>

```
  [DeliveryStreamName](#cfn-iotevents-detectormodel-firehose-deliverystreamname): String
  [Separator](#cfn-iotevents-detectormodel-firehose-separator): String
```

## Properties<a name="aws-properties-iotevents-detectormodel-firehose-properties"></a>

`DeliveryStreamName`  <a name="cfn-iotevents-detectormodel-firehose-deliverystreamname"></a>
The name of the Kinesis Data Firehose delivery stream where the data is written\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Separator`  <a name="cfn-iotevents-detectormodel-firehose-separator"></a>
A character separator that is used to separate records written to the Kinesis Data Firehose delivery stream\. Valid values are: '\\n' \(newline\), '\\t' \(tab\), '\\r\\n' \(Windows newline\), ',' \(comma\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
