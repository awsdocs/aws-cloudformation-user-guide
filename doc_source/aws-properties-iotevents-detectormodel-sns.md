# AWS::IoTEvents::DetectorModel Sns<a name="aws-properties-iotevents-detectormodel-sns"></a>

Sends an Amazon SNS message\.

## Syntax<a name="aws-properties-iotevents-detectormodel-sns-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-sns-syntax.json"></a>

```
{
  "[TargetArn](#cfn-iotevents-detectormodel-sns-targetarn)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-sns-syntax.yaml"></a>

```
  [TargetArn](#cfn-iotevents-detectormodel-sns-targetarn): String
```

## Properties<a name="aws-properties-iotevents-detectormodel-sns-properties"></a>

`TargetArn`  <a name="cfn-iotevents-detectormodel-sns-targetarn"></a>
The ARN of the Amazon SNS target where the message is sent\.  
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
