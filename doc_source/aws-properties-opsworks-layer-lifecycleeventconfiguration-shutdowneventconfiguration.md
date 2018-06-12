# AWS OpsWorks Layer LifeCycleConfiguration ShutdownEventConfiguration<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration-shutdowneventconfiguration"></a>

`ShutdownEventConfiguration` is a property of the [AWS OpsWorks Layer LifeCycleConfiguration](aws-properties-opsworks-layer-lifecycleeventconfiguration.md) property that specifies the shutdown event configuration for a lifecycle event\.

## Syntax<a name="w3ab2c21c14e1565b5"></a>

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

## Properties<a name="w3ab2c21c14e1565b7"></a>

`DelayUntilElbConnectionsDrained`  <a name="cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration-delayuntilelbconnectionsdrained"></a>
Indicates whether to wait for connections to drain from the Elastic Load Balancing load balancers\.  
*Required*: No  
*Type*: Boolean

`ExecutionTimeout`  <a name="cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration-executiontimeout"></a>
The time, in seconds, that AWS OpsWorks waits after a shutdown event has been triggered before shutting down an instance\.  
*Required*: No  
*Type*: Integer