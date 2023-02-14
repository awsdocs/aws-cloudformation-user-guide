# AWS::AppIntegrations::DataIntegration ScheduleConfig<a name="aws-properties-appintegrations-dataintegration-scheduleconfig"></a>

The name of the data and how often it should be pulled from the source\.

## Syntax<a name="aws-properties-appintegrations-dataintegration-scheduleconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appintegrations-dataintegration-scheduleconfig-syntax.json"></a>

```
{
  "[FirstExecutionFrom](#cfn-appintegrations-dataintegration-scheduleconfig-firstexecutionfrom)" : String,
  "[Object](#cfn-appintegrations-dataintegration-scheduleconfig-object)" : String,
  "[ScheduleExpression](#cfn-appintegrations-dataintegration-scheduleconfig-scheduleexpression)" : String
}
```

### YAML<a name="aws-properties-appintegrations-dataintegration-scheduleconfig-syntax.yaml"></a>

```
  [FirstExecutionFrom](#cfn-appintegrations-dataintegration-scheduleconfig-firstexecutionfrom): String
  [Object](#cfn-appintegrations-dataintegration-scheduleconfig-object): String
  [ScheduleExpression](#cfn-appintegrations-dataintegration-scheduleconfig-scheduleexpression): String
```

## Properties<a name="aws-properties-appintegrations-dataintegration-scheduleconfig-properties"></a>

`FirstExecutionFrom`  <a name="cfn-appintegrations-dataintegration-scheduleconfig-firstexecutionfrom"></a>
The start date for objects to import in the first flow run as an Unix/epoch timestamp in milliseconds or in ISO\-8601 format\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Object`  <a name="cfn-appintegrations-dataintegration-scheduleconfig-object"></a>
The name of the object to pull from the data source\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScheduleExpression`  <a name="cfn-appintegrations-dataintegration-scheduleconfig-scheduleexpression"></a>
How often the data should be pulled from data source\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)