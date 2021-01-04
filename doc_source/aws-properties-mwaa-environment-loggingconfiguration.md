# AWS::MWAA::Environment LoggingConfiguration<a name="aws-properties-mwaa-environment-loggingconfiguration"></a>

The Logging Configuration to update of your Amazon MWAA environment\.

## Syntax<a name="aws-properties-mwaa-environment-loggingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mwaa-environment-loggingconfiguration-syntax.json"></a>

```
{
  "[DagProcessingLogs](#cfn-mwaa-environment-loggingconfiguration-dagprocessinglogs)" : ModuleLoggingConfiguration,
  "[SchedulerLogs](#cfn-mwaa-environment-loggingconfiguration-schedulerlogs)" : ModuleLoggingConfiguration,
  "[TaskLogs](#cfn-mwaa-environment-loggingconfiguration-tasklogs)" : ModuleLoggingConfiguration,
  "[WebserverLogs](#cfn-mwaa-environment-loggingconfiguration-webserverlogs)" : ModuleLoggingConfiguration,
  "[WorkerLogs](#cfn-mwaa-environment-loggingconfiguration-workerlogs)" : ModuleLoggingConfiguration
}
```

### YAML<a name="aws-properties-mwaa-environment-loggingconfiguration-syntax.yaml"></a>

```
  [DagProcessingLogs](#cfn-mwaa-environment-loggingconfiguration-dagprocessinglogs): 
    ModuleLoggingConfiguration
  [SchedulerLogs](#cfn-mwaa-environment-loggingconfiguration-schedulerlogs): 
    ModuleLoggingConfiguration
  [TaskLogs](#cfn-mwaa-environment-loggingconfiguration-tasklogs): 
    ModuleLoggingConfiguration
  [WebserverLogs](#cfn-mwaa-environment-loggingconfiguration-webserverlogs): 
    ModuleLoggingConfiguration
  [WorkerLogs](#cfn-mwaa-environment-loggingconfiguration-workerlogs): 
    ModuleLoggingConfiguration
```

## Properties<a name="aws-properties-mwaa-environment-loggingconfiguration-properties"></a>

`DagProcessingLogs`  <a name="cfn-mwaa-environment-loggingconfiguration-dagprocessinglogs"></a>
A JSON blob that provides configuration to use for logging DagProcessingLogs\.  
*Required*: No  
*Type*: [ModuleLoggingConfiguration](aws-properties-mwaa-environment-moduleloggingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchedulerLogs`  <a name="cfn-mwaa-environment-loggingconfiguration-schedulerlogs"></a>
A JSON blob that provides configuration to use for logging SchedulerLogs\.  
*Required*: No  
*Type*: [ModuleLoggingConfiguration](aws-properties-mwaa-environment-moduleloggingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskLogs`  <a name="cfn-mwaa-environment-loggingconfiguration-tasklogs"></a>
A JSON blob that provides configuration to use for logging TaskLogs\.  
*Required*: No  
*Type*: [ModuleLoggingConfiguration](aws-properties-mwaa-environment-moduleloggingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebserverLogs`  <a name="cfn-mwaa-environment-loggingconfiguration-webserverlogs"></a>
A JSON blob that provides configuration to use for logging WebserverLogs\.  
*Required*: No  
*Type*: [ModuleLoggingConfiguration](aws-properties-mwaa-environment-moduleloggingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkerLogs`  <a name="cfn-mwaa-environment-loggingconfiguration-workerlogs"></a>
A JSON blob that provides configuration to use for logging WorkerLogs\.  
*Required*: No  
*Type*: [ModuleLoggingConfiguration](aws-properties-mwaa-environment-moduleloggingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)