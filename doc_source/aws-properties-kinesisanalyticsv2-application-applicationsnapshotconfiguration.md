# Amazon Kinesis Data Analytics Application ApplicationSnapshotConfiguration<a name="aws-properties-kinesisanalyticsv2-application-applicationsnapshotconfiguration"></a>

<a name="aws-properties-kinesisanalyticsv2-application-applicationsnapshotconfiguration-description"></a>The `ApplicationSnapshotConfiguration` property type describes whether snapshots are enabled for a Java\-based Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-application-applicationsnapshotconfiguration-inheritance"></a> `ApplicationSnapshotConfiguration` is a property of the [ApplicationConfiguration](aws-properties-kinesisanalyticsv2-application-applicationconfiguration.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-applicationsnapshotconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-applicationsnapshotconfiguration-syntax.json"></a>

```
{
  "[SnapshotsEnabled](#cfn-kinesisanalyticsv2-application-applicationsnapshotconfiguration-snapshotsenabled)" : Boolean
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-applicationsnapshotconfiguration-syntax.yaml"></a>

```
[SnapshotsEnabled](#cfn-kinesisanalyticsv2-application-applicationsnapshotconfiguration-snapshotsenabled): Boolean
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-applicationsnapshotconfiguration-properties"></a>

`SnapshotsEnabled`  <a name="cfn-kinesisanalyticsv2-application-applicationsnapshotconfiguration-snapshotsenabled"></a>
Describes whether snapshots are enabled for a Java\-based Kinesis Data Analytics application\.  
 *Required*: Yes  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 