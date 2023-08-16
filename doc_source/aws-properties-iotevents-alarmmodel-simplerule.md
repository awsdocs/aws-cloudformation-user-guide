# AWS::IoTEvents::AlarmModel SimpleRule<a name="aws-properties-iotevents-alarmmodel-simplerule"></a>

A rule that compares an input property value to a threshold value with a comparison operator\.

## Syntax<a name="aws-properties-iotevents-alarmmodel-simplerule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-alarmmodel-simplerule-syntax.json"></a>

```
{
  "[ComparisonOperator](#cfn-iotevents-alarmmodel-simplerule-comparisonoperator)" : String,
  "[InputProperty](#cfn-iotevents-alarmmodel-simplerule-inputproperty)" : String,
  "[Threshold](#cfn-iotevents-alarmmodel-simplerule-threshold)" : String
}
```

### YAML<a name="aws-properties-iotevents-alarmmodel-simplerule-syntax.yaml"></a>

```
  [ComparisonOperator](#cfn-iotevents-alarmmodel-simplerule-comparisonoperator): String
  [InputProperty](#cfn-iotevents-alarmmodel-simplerule-inputproperty): String
  [Threshold](#cfn-iotevents-alarmmodel-simplerule-threshold): String
```

## Properties<a name="aws-properties-iotevents-alarmmodel-simplerule-properties"></a>

`ComparisonOperator`  <a name="cfn-iotevents-alarmmodel-simplerule-comparisonoperator"></a>
The comparison operator\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `EQUAL | GREATER | GREATER_OR_EQUAL | LESS | LESS_OR_EQUAL | NOT_EQUAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputProperty`  <a name="cfn-iotevents-alarmmodel-simplerule-inputproperty"></a>
The value on the left side of the comparison operator\. You can specify an AWS IoT Events input attribute as an input property\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Threshold`  <a name="cfn-iotevents-alarmmodel-simplerule-threshold"></a>
The value on the right side of the comparison operator\. You can enter a number or specify an AWS IoT Events input attribute\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)