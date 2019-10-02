# AWS::KinesisAnalyticsV2::Application JSONMappingParameters<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters"></a>

For an SQL\-based Amazon Kinesis Data Analytics application, provides additional mapping information when JSON is the record format on the streaming source\.

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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters--seealso"></a>
+  [JSONMappingParameters](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_JSONMappingParameters.html) in the *Amazon Kinesis Data Analytics API Reference* 

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
