# AWS::CustomerProfiles::Integration TriggerProperties<a name="aws-properties-customerprofiles-integration-triggerproperties"></a>

Specifies the configuration details that control the trigger for a flow\. Currently, these settings only apply to the Scheduled trigger type\.

## Syntax<a name="aws-properties-customerprofiles-integration-triggerproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-integration-triggerproperties-syntax.json"></a>

```
{
  "[Scheduled](#cfn-customerprofiles-integration-triggerproperties-scheduled)" : ScheduledTriggerProperties
}
```

### YAML<a name="aws-properties-customerprofiles-integration-triggerproperties-syntax.yaml"></a>

```
  [Scheduled](#cfn-customerprofiles-integration-triggerproperties-scheduled): 
    ScheduledTriggerProperties
```

## Properties<a name="aws-properties-customerprofiles-integration-triggerproperties-properties"></a>

`Scheduled`  <a name="cfn-customerprofiles-integration-triggerproperties-scheduled"></a>
Specifies the configuration details of a schedule\-triggered flow that you define\.  
*Required*: No  
*Type*: [ScheduledTriggerProperties](aws-properties-customerprofiles-integration-scheduledtriggerproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)