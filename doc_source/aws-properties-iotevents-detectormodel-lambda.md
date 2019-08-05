# AWS::IoTEvents::DetectorModel Lambda<a name="aws-properties-iotevents-detectormodel-lambda"></a>

Calls an AWS Lambda function, passing in information about the detector model instance and the event which triggered the action\.

## Syntax<a name="aws-properties-iotevents-detectormodel-lambda-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-lambda-syntax.json"></a>

```
{
  "[FunctionArn](#cfn-iotevents-detectormodel-lambda-functionarn)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-lambda-syntax.yaml"></a>

```
  [FunctionArn](#cfn-iotevents-detectormodel-lambda-functionarn): String
```

## Properties<a name="aws-properties-iotevents-detectormodel-lambda-properties"></a>

`FunctionArn`  <a name="cfn-iotevents-detectormodel-lambda-functionarn"></a>
The ARN of the AWS Lambda function which is executed\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
