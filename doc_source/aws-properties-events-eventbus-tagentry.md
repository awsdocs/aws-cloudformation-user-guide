# AWS::Events::EventBus TagEntry<a name="aws-properties-events-eventbus-tagentry"></a>

A key\-value pair associated with an AWS resource\. In EventBridge, rules and event buses support tagging\.

## Syntax<a name="aws-properties-events-eventbus-tagentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-eventbus-tagentry-syntax.json"></a>

```
{
  "[Key](#cfn-events-eventbus-tagentry-key)" : String,
  "[Value](#cfn-events-eventbus-tagentry-value)" : String
}
```

### YAML<a name="aws-properties-events-eventbus-tagentry-syntax.yaml"></a>

```
  [Key](#cfn-events-eventbus-tagentry-key): String
  [Value](#cfn-events-eventbus-tagentry-value): String
```

## Properties<a name="aws-properties-events-eventbus-tagentry-properties"></a>

`Key`  <a name="cfn-events-eventbus-tagentry-key"></a>
A string you can use to assign a value\. The combination of tag keys and values can help you organize and categorize your resources\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-events-eventbus-tagentry-value"></a>
The value for the specified tag key\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)