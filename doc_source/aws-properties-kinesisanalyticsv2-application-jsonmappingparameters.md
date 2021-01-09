# AWS::KinesisAnalyticsV2::Application JSONMappingParameters<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters"></a>

For a SQL\-based Kinesis Data Analytics application, provides additional mapping information when JSON is the record format on the streaming source\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters-syntax.json"></a>

```
{
  "[RecordRowPath](#cfn-kinesisanalyticsv2-application-jsonmappingparameters-recordrowpath)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters-syntax.yaml"></a>

```
  [RecordRowPath](#cfn-kinesisanalyticsv2-application-jsonmappingparameters-recordrowpath): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters-properties"></a>

`RecordRowPath`  <a name="cfn-kinesisanalyticsv2-application-jsonmappingparameters-recordrowpath"></a>
The path to the top\-level parent that contains the records\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `65535`  
*Pattern*: `^(?=^\$)(?=^\S+$).*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters--seealso"></a>
+  [JSONMappingParameters](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_JSONMappingParameters.html) in the *Amazon Kinesis Data Analytics API Reference* 

