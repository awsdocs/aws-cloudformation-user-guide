# AWS::IoTAnalytics::Dataset IotEventsDestinationConfiguration<a name="aws-properties-iotanalytics-dataset-ioteventsdestinationconfiguration"></a>

Configuration information for delivery of dataset contents to AWS IoT Events\.

## Syntax<a name="aws-properties-iotanalytics-dataset-ioteventsdestinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-ioteventsdestinationconfiguration-syntax.json"></a>

```
{
  "[InputName](#cfn-iotanalytics-dataset-ioteventsdestinationconfiguration-inputname)" : String,
  "[RoleArn](#cfn-iotanalytics-dataset-ioteventsdestinationconfiguration-rolearn)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-ioteventsdestinationconfiguration-syntax.yaml"></a>

```
  [InputName](#cfn-iotanalytics-dataset-ioteventsdestinationconfiguration-inputname): String
  [RoleArn](#cfn-iotanalytics-dataset-ioteventsdestinationconfiguration-rolearn): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-ioteventsdestinationconfiguration-properties"></a>

`InputName`  <a name="cfn-iotanalytics-dataset-ioteventsdestinationconfiguration-inputname"></a>
The name of the AWS IoT Events input to which dataset contents are delivered\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iotanalytics-dataset-ioteventsdestinationconfiguration-rolearn"></a>
The ARN of the role that grants AWS IoT Analytics permission to deliver dataset contents to an AWS IoT Events input\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)