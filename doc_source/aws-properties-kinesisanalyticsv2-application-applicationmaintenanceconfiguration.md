# AWS::KinesisAnalyticsV2::Application ApplicationMaintenanceConfiguration<a name="aws-properties-kinesisanalyticsv2-application-applicationmaintenanceconfiguration"></a>

Specifies the maintence window parameters for a Kinesis Data Analytics application\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-applicationmaintenanceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-applicationmaintenanceconfiguration-syntax.json"></a>

```
{
  "[ApplicationMaintenanceWindowStartTime](#cfn-kinesisanalyticsv2-application-applicationmaintenanceconfiguration-applicationmaintenancewindowstarttime)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-applicationmaintenanceconfiguration-syntax.yaml"></a>

```
  [ApplicationMaintenanceWindowStartTime](#cfn-kinesisanalyticsv2-application-applicationmaintenanceconfiguration-applicationmaintenancewindowstarttime): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-applicationmaintenanceconfiguration-properties"></a>

`ApplicationMaintenanceWindowStartTime`  <a name="cfn-kinesisanalyticsv2-application-applicationmaintenanceconfiguration-applicationmaintenancewindowstarttime"></a>
Specifies the start time of the maintence window\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)