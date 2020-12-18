# AWS::KinesisAnalyticsV2::Application SqlApplicationConfiguration<a name="aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration"></a>

Describes the inputs, outputs, and reference data sources for a SQL\-based Kinesis Data Analytics application\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration-syntax.json"></a>

```
{
  "[Inputs](#cfn-kinesisanalyticsv2-application-sqlapplicationconfiguration-inputs)" : [ Input, ... ]
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration-syntax.yaml"></a>

```
  [Inputs](#cfn-kinesisanalyticsv2-application-sqlapplicationconfiguration-inputs): 
    - Input
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration-properties"></a>

`Inputs`  <a name="cfn-kinesisanalyticsv2-application-sqlapplicationconfiguration-inputs"></a>
The array of [Input](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_Input.html) objects describing the input streams used by the application\.  
*Required*: No  
*Type*: List of [Input](aws-properties-kinesisanalyticsv2-application-input.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-sqlapplicationconfiguration--seealso"></a>
+  [SqlApplicationConfiguration](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_SqlApplicationConfiguration.html) in the *Amazon Kinesis Data Analytics API Reference* 

