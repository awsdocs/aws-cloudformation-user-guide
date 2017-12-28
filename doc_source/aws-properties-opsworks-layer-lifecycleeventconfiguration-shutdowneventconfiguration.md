# AWS OpsWorks Layer LifeCycleConfiguration ShutdownEventConfiguration<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration-shutdowneventconfiguration"></a>

`ShutdownEventConfiguration` is a property of the [AWS OpsWorks Layer LifeCycleConfiguration](aws-properties-opsworks-layer-lifecycleeventconfiguration.md) property that specifies the shutdown event configuration for a lifecycle event\.

## Syntax<a name="w3ab2c21c14e1359b5"></a>

### JSON<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration-shutdowneventconfiguration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration-delayuntilelbconnectionsdrained)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration-executiontimeout)" : Integer
}
```

### YAML<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration-shutdowneventconfiguration-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration-delayuntilelbconnectionsdrained): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration-executiontimeout): Integer
```

## Properties<a name="w3ab2c21c14e1359b7"></a>

`DelayUntilElbConnectionsDrained`  
Indicates whether to wait for connections to drain from the Elastic Load Balancing load balancers\.  
*Required: *No  
*Type*: Boolean

`ExecutionTimeout`  
The time, in seconds, that AWS OpsWorks waits after a shutdown event has been triggered before shutting down an instance\.  
*Required: *No  
*Type*: Integer