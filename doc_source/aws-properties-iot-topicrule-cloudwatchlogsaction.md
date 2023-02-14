# AWS::IoT::TopicRule CloudwatchLogsAction<a name="aws-properties-iot-topicrule-cloudwatchlogsaction"></a>

Describes an action that updates a CloudWatch log\.

## Syntax<a name="aws-properties-iot-topicrule-cloudwatchlogsaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-cloudwatchlogsaction-syntax.json"></a>

```
{
  "[LogGroupName](#cfn-iot-topicrule-cloudwatchlogsaction-loggroupname)" : String,
  "[RoleArn](#cfn-iot-topicrule-cloudwatchlogsaction-rolearn)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-cloudwatchlogsaction-syntax.yaml"></a>

```
  [LogGroupName](#cfn-iot-topicrule-cloudwatchlogsaction-loggroupname): String
  [RoleArn](#cfn-iot-topicrule-cloudwatchlogsaction-rolearn): String
```

## Properties<a name="aws-properties-iot-topicrule-cloudwatchlogsaction-properties"></a>

`LogGroupName`  <a name="cfn-iot-topicrule-cloudwatchlogsaction-loggroupname"></a>
The CloudWatch log name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-cloudwatchlogsaction-rolearn"></a>
The IAM role that allows access to the CloudWatch log\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)