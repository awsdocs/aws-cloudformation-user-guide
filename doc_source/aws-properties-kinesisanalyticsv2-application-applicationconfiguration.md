# AWS::KinesisAnalyticsV2::Application ApplicationConfiguration<a name="aws-properties-kinesisanalyticsv2-application-applicationconfiguration"></a>

Specifies the creation parameters for a Kinesis Data Analytics application\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-applicationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-applicationconfiguration-syntax.json"></a>

```
{
  "[ApplicationCodeConfiguration](#cfn-kinesisanalyticsv2-application-applicationconfiguration-applicationcodeconfiguration)" : ApplicationCodeConfiguration,
  "[ApplicationSnapshotConfiguration](#cfn-kinesisanalyticsv2-application-applicationconfiguration-applicationsnapshotconfiguration)" : ApplicationSnapshotConfiguration,
  "[EnvironmentProperties](#cfn-kinesisanalyticsv2-application-applicationconfiguration-environmentproperties)" : EnvironmentProperties,
  "[FlinkApplicationConfiguration](#cfn-kinesisanalyticsv2-application-applicationconfiguration-flinkapplicationconfiguration)" : FlinkApplicationConfiguration,
  "[SqlApplicationConfiguration](#cfn-kinesisanalyticsv2-application-applicationconfiguration-sqlapplicationconfiguration)" : SqlApplicationConfiguration
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-applicationconfiguration-syntax.yaml"></a>

```
  [ApplicationCodeConfiguration](#cfn-kinesisanalyticsv2-application-applicationconfiguration-applicationcodeconfiguration): 
    ApplicationCodeConfiguration
  [ApplicationSnapshotConfiguration](#cfn-kinesisanalyticsv2-application-applicationconfiguration-applicationsnapshotconfiguration): 
    ApplicationSnapshotConfiguration
  [EnvironmentProperties](#cfn-kinesisanalyticsv2-application-applicationconfiguration-environmentproperties): 
    EnvironmentProperties
  [FlinkApplicationConfiguration](#cfn-kinesisanalyticsv2-application-applicationconfiguration-flinkapplicationconfiguration): 
    FlinkApplicationConfiguration
  [SqlApplicationConfiguration](#cfn-kinesisanalyticsv2-application-applicationconfiguration-sqlapplicationconfiguration): 
    SqlApplicationConfiguration
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-applicationconfiguration-properties"></a>

`ApplicationCodeConfiguration`  <a name="cfn-kinesisanalyticsv2-application-applicationconfiguration-applicationcodeconfiguration"></a>
The code location and type parameters for a Flink\-based Kinesis Data Analytics application\.  
*Required*: Conditional  
*Type*: [ApplicationCodeConfiguration](aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApplicationSnapshotConfiguration`  <a name="cfn-kinesisanalyticsv2-application-applicationconfiguration-applicationsnapshotconfiguration"></a>
Describes whether snapshots are enabled for a Flink\-based Kinesis Data Analytics application\.  
*Required*: No  
*Type*: [ApplicationSnapshotConfiguration](aws-properties-kinesisanalyticsv2-application-applicationsnapshotconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentProperties`  <a name="cfn-kinesisanalyticsv2-application-applicationconfiguration-environmentproperties"></a>
Describes execution properties for a Flink\-based Kinesis Data Analytics application\.  
*Required*: No  
*Type*: [EnvironmentProperties](aws-properties-kinesisanalyticsv2-application-environmentproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FlinkApplicationConfiguration`  <a name="cfn-kinesisanalyticsv2-application-applicationconfiguration-flinkapplicationconfiguration"></a>
The creation and update parameters for a Flink\-based Kinesis Data Analytics application\.  
*Required*: No  
*Type*: [FlinkApplicationConfiguration](aws-properties-kinesisanalyticsv2-application-flinkapplicationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqlApplicationConfiguration`  <a name="cfn-kinesisanalyticsv2-application-applicationconfiguration-sqlapplicationconfiguration"></a>
The creation and update parameters for a SQL\-based Kinesis Data Analytics application\.  
*Required*: No  
*Type*: [SqlApplicationConfiguration](aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-applicationconfiguration--seealso"></a>
+  [ApplicationConfiguration](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_ApplicationConfiguration.html) in the *Amazon Kinesis Data Analytics API Reference* 

