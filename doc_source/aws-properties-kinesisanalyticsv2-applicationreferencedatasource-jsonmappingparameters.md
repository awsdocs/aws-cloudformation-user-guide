# AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource JSONMappingParameters<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters"></a>

For a SQL\-based Kinesis Data Analytics application, provides additional mapping information when JSON is the record format on the streaming source\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-syntax.json"></a>

```
{
  "[RecordRowPath](#cfn-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-recordrowpath)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-syntax.yaml"></a>

```
  [RecordRowPath](#cfn-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-recordrowpath): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-properties"></a>

`RecordRowPath`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-recordrowpath"></a>
The path to the top\-level parent that contains the records\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `65535`  
*Pattern*: `^(?=^\$)(?=^\S+$).*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters--seealso"></a>
+  [JSONMappingParameters](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_JSONMappingParameters.html) in the *Amazon Kinesis Data Analytics API Reference* 

