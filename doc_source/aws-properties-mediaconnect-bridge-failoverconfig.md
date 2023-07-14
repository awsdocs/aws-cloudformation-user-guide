# AWS::MediaConnect::Bridge FailoverConfig<a name="aws-properties-mediaconnect-bridge-failoverconfig"></a>

The settings for source failover\.

## Syntax<a name="aws-properties-mediaconnect-bridge-failoverconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconnect-bridge-failoverconfig-syntax.json"></a>

```
{
  "[FailoverMode](#cfn-mediaconnect-bridge-failoverconfig-failovermode)" : String,
  "[SourcePriority](#cfn-mediaconnect-bridge-failoverconfig-sourcepriority)" : SourcePriority,
  "[State](#cfn-mediaconnect-bridge-failoverconfig-state)" : String
}
```

### YAML<a name="aws-properties-mediaconnect-bridge-failoverconfig-syntax.yaml"></a>

```
  [FailoverMode](#cfn-mediaconnect-bridge-failoverconfig-failovermode): String
  [SourcePriority](#cfn-mediaconnect-bridge-failoverconfig-sourcepriority): 
    SourcePriority
  [State](#cfn-mediaconnect-bridge-failoverconfig-state): String
```

## Properties<a name="aws-properties-mediaconnect-bridge-failoverconfig-properties"></a>

`FailoverMode`  <a name="cfn-mediaconnect-bridge-failoverconfig-failovermode"></a>
The type of failover you choose for this flow\. MERGE combines the source streams into a single stream, allowing graceful recovery from any single\-source loss\. FAILOVER allows switching between different streams\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourcePriority`  <a name="cfn-mediaconnect-bridge-failoverconfig-sourcepriority"></a>
The priority you want to assign to a source\. You can have a primary stream and a backup stream or two equally prioritized streams\. This setting only applies when Failover Mode is set to FAILOVER\.  
*Required*: No  
*Type*: [SourcePriority](aws-properties-mediaconnect-bridge-sourcepriority.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-mediaconnect-bridge-failoverconfig-state"></a>
The state of source failover on the flow\. If the state is inactive, the flow can have only one source\. If the state is active, the flow can have one or two sources\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)