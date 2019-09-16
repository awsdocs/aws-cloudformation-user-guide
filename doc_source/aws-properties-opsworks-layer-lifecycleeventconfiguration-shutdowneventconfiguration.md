# AWS::OpsWorks::Layer ShutdownEventConfiguration<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration-shutdowneventconfiguration"></a>

The Shutdown event configuration\.

## Syntax<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration-shutdowneventconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration-shutdowneventconfiguration-syntax.json"></a>

```
{
  "[DelayUntilElbConnectionsDrained](#cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration-delayuntilelbconnectionsdrained)" : Boolean,
  "[ExecutionTimeout](#cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration-executiontimeout)" : Integer
}
```

### YAML<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration-shutdowneventconfiguration-syntax.yaml"></a>

```
  [DelayUntilElbConnectionsDrained](#cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration-delayuntilelbconnectionsdrained): Boolean
  [ExecutionTimeout](#cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration-executiontimeout): Integer
```

## Properties<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration-shutdowneventconfiguration-properties"></a>

`DelayUntilElbConnectionsDrained`  <a name="cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration-delayuntilelbconnectionsdrained"></a>
Whether to enable Elastic Load Balancing connection draining\. For more information, see [Connection Draining](https://docs.aws.amazon.com/ElasticLoadBalancing/latest/DeveloperGuide/TerminologyandKeyConcepts.html#conn-drain)   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExecutionTimeout`  <a name="cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration-executiontimeout"></a>
The time, in seconds, that AWS OpsWorks Stacks will wait after triggering a Shutdown event before shutting down an instance\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)