# AWS::CustomerProfiles::Integration TriggerConfig<a name="aws-properties-customerprofiles-integration-triggerconfig"></a>

The trigger settings that determine how and when Amazon AppFlow runs the specified flow\.

## Syntax<a name="aws-properties-customerprofiles-integration-triggerconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-integration-triggerconfig-syntax.json"></a>

```
{
  "[TriggerProperties](#cfn-customerprofiles-integration-triggerconfig-triggerproperties)" : TriggerProperties,
  "[TriggerType](#cfn-customerprofiles-integration-triggerconfig-triggertype)" : String
}
```

### YAML<a name="aws-properties-customerprofiles-integration-triggerconfig-syntax.yaml"></a>

```
  [TriggerProperties](#cfn-customerprofiles-integration-triggerconfig-triggerproperties): 
    TriggerProperties
  [TriggerType](#cfn-customerprofiles-integration-triggerconfig-triggertype): String
```

## Properties<a name="aws-properties-customerprofiles-integration-triggerconfig-properties"></a>

`TriggerProperties`  <a name="cfn-customerprofiles-integration-triggerconfig-triggerproperties"></a>
Specifies the configuration details of a schedule\-triggered flow that you define\. Currently, these settings only apply to the Scheduled trigger type\.  
*Required*: No  
*Type*: [TriggerProperties](aws-properties-customerprofiles-integration-triggerproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TriggerType`  <a name="cfn-customerprofiles-integration-triggerconfig-triggertype"></a>
Specifies the type of flow trigger\. It can be OnDemand, Scheduled, or Event\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Event | OnDemand | Scheduled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)