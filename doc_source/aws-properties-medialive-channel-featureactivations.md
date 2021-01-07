# AWS::MediaLive::Channel FeatureActivations<a name="aws-properties-medialive-channel-featureactivations"></a>

Feature Activations

## Syntax<a name="aws-properties-medialive-channel-featureactivations-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-featureactivations-syntax.json"></a>

```
{
  "[InputPrepareScheduleActions](#cfn-medialive-channel-featureactivations-inputpreparescheduleactions)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-featureactivations-syntax.yaml"></a>

```
  [InputPrepareScheduleActions](#cfn-medialive-channel-featureactivations-inputpreparescheduleactions): String
```

## Properties<a name="aws-properties-medialive-channel-featureactivations-properties"></a>

`InputPrepareScheduleActions`  <a name="cfn-medialive-channel-featureactivations-inputpreparescheduleactions"></a>
Enables the Input Prepare feature\. You can create Input Prepare actions in the schedule only if this feature is enabled\. If you disable the feature on an existing schedule, make sure that you first delete all input prepare actions from the schedule\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)