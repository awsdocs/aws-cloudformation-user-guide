# AWS::Scheduler::Schedule EventBridgeParameters<a name="aws-properties-scheduler-schedule-eventbridgeparameters"></a>

The templated target type for the EventBridge [https://docs.aws.amazon.com/eventbridge/latest/APIReference/API_PutEvents.html](https://docs.aws.amazon.com/eventbridge/latest/APIReference/API_PutEvents.html) API operation\.

## Syntax<a name="aws-properties-scheduler-schedule-eventbridgeparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-scheduler-schedule-eventbridgeparameters-syntax.json"></a>

```
{
  "[DetailType](#cfn-scheduler-schedule-eventbridgeparameters-detailtype)" : String,
  "[Source](#cfn-scheduler-schedule-eventbridgeparameters-source)" : String
}
```

### YAML<a name="aws-properties-scheduler-schedule-eventbridgeparameters-syntax.yaml"></a>

```
  [DetailType](#cfn-scheduler-schedule-eventbridgeparameters-detailtype): String
  [Source](#cfn-scheduler-schedule-eventbridgeparameters-source): String
```

## Properties<a name="aws-properties-scheduler-schedule-eventbridgeparameters-properties"></a>

`DetailType`  <a name="cfn-scheduler-schedule-eventbridgeparameters-detailtype"></a>
A free\-form string, with a maximum of 128 characters, used to decide what fields to expect in the event detail\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source`  <a name="cfn-scheduler-schedule-eventbridgeparameters-source"></a>
The source of the event\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)