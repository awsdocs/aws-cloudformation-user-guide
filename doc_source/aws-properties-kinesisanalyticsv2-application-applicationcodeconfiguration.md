# AWS::KinesisAnalyticsV2::Application ApplicationCodeConfiguration<a name="aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration"></a>

Describes code configuration for a Flink\-based Kinesis Data Analytics application\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration-syntax.json"></a>

```
{
  "[CodeContent](#cfn-kinesisanalyticsv2-application-applicationcodeconfiguration-codecontent)" : CodeContent,
  "[CodeContentType](#cfn-kinesisanalyticsv2-application-applicationcodeconfiguration-codecontenttype)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration-syntax.yaml"></a>

```
  [CodeContent](#cfn-kinesisanalyticsv2-application-applicationcodeconfiguration-codecontent): 
    CodeContent
  [CodeContentType](#cfn-kinesisanalyticsv2-application-applicationcodeconfiguration-codecontenttype): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration-properties"></a>

`CodeContent`  <a name="cfn-kinesisanalyticsv2-application-applicationcodeconfiguration-codecontent"></a>
The location and type of the application code\.  
*Required*: Yes  
*Type*: [CodeContent](aws-properties-kinesisanalyticsv2-application-codecontent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CodeContentType`  <a name="cfn-kinesisanalyticsv2-application-applicationcodeconfiguration-codecontenttype"></a>
Specifies whether the code content is in text or zip format\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `PLAINTEXT | ZIPFILE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-applicationcodeconfiguration--seealso"></a>
+  [ApplicationCodeConfiguration](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_ApplicationCodeConfiguration.html) in the *Amazon Kinesis Data Analytics API Reference* 

