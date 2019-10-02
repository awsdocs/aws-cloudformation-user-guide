# AWS::KinesisAnalyticsV2::Application ApplicationSnapshotConfiguration<a name="aws-properties-kinesisanalyticsv2-application-applicationsnapshotconfiguration"></a>

Describes whether snapshots are enabled for a Java\-based Kinesis Data Analytics application\.

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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-kinesisanalyticsv2-application-applicationsnapshotconfiguration--seealso"></a>
+  [ApplicationSnapshotConfiguration](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_ApplicationSnapshotConfiguration.html) in the *Amazon Kinesis Data Analytics API Reference* 

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-2`
