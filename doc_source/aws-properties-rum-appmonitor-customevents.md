# AWS::RUM::AppMonitor CustomEvents<a name="aws-properties-rum-appmonitor-customevents"></a>

This structure specifies whether this app monitor allows the web client to define and send custom events\.

## Syntax<a name="aws-properties-rum-appmonitor-customevents-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rum-appmonitor-customevents-syntax.json"></a>

```
{
  "[Status](#cfn-rum-appmonitor-customevents-status)" : String
}
```

### YAML<a name="aws-properties-rum-appmonitor-customevents-syntax.yaml"></a>

```
  [Status](#cfn-rum-appmonitor-customevents-status): String
```

## Properties<a name="aws-properties-rum-appmonitor-customevents-properties"></a>

`Status`  <a name="cfn-rum-appmonitor-customevents-status"></a>
Set this to `ENABLED` to allow the web client to send custom events for this app monitor\.  
Valid values are `ENABLED` and `DISABLED`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)