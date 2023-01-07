# AWS::OpsWorks::Layer LifecycleEventConfiguration<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration"></a>

Specifies the lifecycle event configuration

## Syntax<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration-syntax.json"></a>

```
{
  "[ShutdownEventConfiguration](#cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration)" : ShutdownEventConfiguration
}
```

### YAML<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration-syntax.yaml"></a>

```
  [ShutdownEventConfiguration](#cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration): 
    ShutdownEventConfiguration
```

## Properties<a name="aws-properties-opsworks-layer-lifecycleeventconfiguration-properties"></a>

`ShutdownEventConfiguration`  <a name="cfn-opsworks-layer-lifecycleconfiguration-shutdowneventconfiguration"></a>
The Shutdown event configuration\.  
*Required*: No  
*Type*: [ShutdownEventConfiguration](aws-properties-opsworks-layer-lifecycleeventconfiguration-shutdowneventconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)