# AWS::MediaConnect::Flow FailoverConfig<a name="aws-properties-mediaconnect-flow-failoverconfig"></a>

The settings for source failover\.

## Syntax<a name="aws-properties-mediaconnect-flow-failoverconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconnect-flow-failoverconfig-syntax.json"></a>

```
{
  "[RecoveryWindow](#cfn-mediaconnect-flow-failoverconfig-recoverywindow)" : Integer,
  "[State](#cfn-mediaconnect-flow-failoverconfig-state)" : String
}
```

### YAML<a name="aws-properties-mediaconnect-flow-failoverconfig-syntax.yaml"></a>

```
  [RecoveryWindow](#cfn-mediaconnect-flow-failoverconfig-recoverywindow): Integer
  [State](#cfn-mediaconnect-flow-failoverconfig-state): String
```

## Properties<a name="aws-properties-mediaconnect-flow-failoverconfig-properties"></a>

`RecoveryWindow`  <a name="cfn-mediaconnect-flow-failoverconfig-recoverywindow"></a>
The size of the buffer \(delay\) that the service maintains\. A larger buffer means a longer delay in transmitting the stream, but more room for error correction\. A smaller buffer means a shorter delay, but less room for error correction\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-mediaconnect-flow-failoverconfig-state"></a>
The state of source failover on the flow\. If the state is disabled, the flow can have only one source\. If the state is enabled, the flow can have one or two sources\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)