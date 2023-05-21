# AWS::AppFlow::Flow TriggerConfig<a name="aws-properties-appflow-flow-triggerconfig"></a>

 The trigger settings that determine how and when Amazon AppFlow runs the specified flow\. 

## Syntax<a name="aws-properties-appflow-flow-triggerconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-triggerconfig-syntax.json"></a>

```
{
  "[TriggerProperties](#cfn-appflow-flow-triggerconfig-triggerproperties)" : ScheduledTriggerProperties,
  "[TriggerType](#cfn-appflow-flow-triggerconfig-triggertype)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-triggerconfig-syntax.yaml"></a>

```
  [TriggerProperties](#cfn-appflow-flow-triggerconfig-triggerproperties): 
    ScheduledTriggerProperties
  [TriggerType](#cfn-appflow-flow-triggerconfig-triggertype): String
```

## Properties<a name="aws-properties-appflow-flow-triggerconfig-properties"></a>

`TriggerProperties`  <a name="cfn-appflow-flow-triggerconfig-triggerproperties"></a>
 Specifies the configuration details of a schedule\-triggered flow as defined by the user\. Currently, these settings only apply to the `Scheduled` trigger type\.   
*Required*: No  
*Type*: [ScheduledTriggerProperties](aws-properties-appflow-flow-scheduledtriggerproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TriggerType`  <a name="cfn-appflow-flow-triggerconfig-triggertype"></a>
 Specifies the type of flow trigger\. This can be `OnDemand`, `Scheduled`, or `Event`\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `Event | OnDemand | Scheduled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-triggerconfig--seealso"></a>
+ [TriggerConfig](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_TriggerConfig.html) in the *Amazon AppFlow API Reference*\.

