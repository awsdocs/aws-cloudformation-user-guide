# AWS::DLM::LifecyclePolicy EventSource<a name="aws-properties-dlm-lifecyclepolicy-eventsource"></a>

Specifies an event that triggers an event\-based policy\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-eventsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-eventsource-syntax.json"></a>

```
{
  "[Parameters](#cfn-dlm-lifecyclepolicy-eventsource-parameters)" : EventParameters,
  "[Type](#cfn-dlm-lifecyclepolicy-eventsource-type)" : String
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-eventsource-syntax.yaml"></a>

```
  [Parameters](#cfn-dlm-lifecyclepolicy-eventsource-parameters): 
    EventParameters
  [Type](#cfn-dlm-lifecyclepolicy-eventsource-type): String
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-eventsource-properties"></a>

`Parameters`  <a name="cfn-dlm-lifecyclepolicy-eventsource-parameters"></a>
Information about the event\.  
*Required*: No  
*Type*: [EventParameters](aws-properties-dlm-lifecyclepolicy-eventparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-dlm-lifecyclepolicy-eventsource-type"></a>
The source of the event\. Currently only managed AWS CloudWatch Events rules are supported\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `MANAGED_CWE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)