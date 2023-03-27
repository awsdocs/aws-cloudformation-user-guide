# AWS::IoTEvents::AlarmModel Payload<a name="aws-properties-iotevents-alarmmodel-payload"></a>

Information needed to configure the payload\.

By default, AWS IoT Events generates a standard payload in JSON for any action\. This action payload contains all attribute\-value pairs that have the information about the detector model instance and the event triggered the action\. To configure the action payload, you can use `contentExpression`\.

## Syntax<a name="aws-properties-iotevents-alarmmodel-payload-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-alarmmodel-payload-syntax.json"></a>

```
{
  "[ContentExpression](#cfn-iotevents-alarmmodel-payload-contentexpression)" : String,
  "[Type](#cfn-iotevents-alarmmodel-payload-type)" : String
}
```

### YAML<a name="aws-properties-iotevents-alarmmodel-payload-syntax.yaml"></a>

```
  [ContentExpression](#cfn-iotevents-alarmmodel-payload-contentexpression): String
  [Type](#cfn-iotevents-alarmmodel-payload-type): String
```

## Properties<a name="aws-properties-iotevents-alarmmodel-payload-properties"></a>

`ContentExpression`  <a name="cfn-iotevents-alarmmodel-payload-contentexpression"></a>
The content of the payload\. You can use a string expression that includes quoted strings \(`'<string>'`\), variables \(`$variable.<variable-name>`\), input values \(`$input.<input-name>.<path-to-datum>`\), string concatenations, and quoted strings that contain `${}` as the content\. The recommended maximum size of a content expression is 1 KB\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-iotevents-alarmmodel-payload-type"></a>
The value of the payload type can be either `STRING` or `JSON`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `JSON | STRING`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)