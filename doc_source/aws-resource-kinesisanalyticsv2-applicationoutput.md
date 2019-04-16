# AWS::KinesisAnalyticsV2::ApplicationOutput<a name="aws-resource-kinesisanalyticsv2-applicationoutput"></a>

The `AWS::KinesisAnalyticsV2::ApplicationOutput` resource describes a SQL\-based Amazon Kinesis Data Analytics application's output configuration\. 

## Syntax<a name="aws-resource-kinesisanalyticsv2-applicationoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisanalyticsv2-applicationoutput-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisAnalyticsV2::ApplicationOutput",
  "Properties" : {
    "[ApplicationName](#cfn-kinesisanalyticsv2-applicationoutput-applicationname)" : String,
    "[Output](#cfn-kinesisanalyticsv2-applicationoutput-output)" : [*Output*](aws-properties-kinesisanalyticsv2-applicationoutput-output.md)
  }
}
```

### YAML<a name="aws-resource-kinesisanalyticsv2-applicationoutput-syntax.yaml"></a>

```
Type: "AWS::KinesisAnalyticsV2::ApplicationOutput"
Properties:
  [ApplicationName](#cfn-kinesisanalyticsv2-applicationoutput-applicationname): String
  [Output](#cfn-kinesisanalyticsv2-applicationoutput-output): [*Output*](aws-properties-kinesisanalyticsv2-applicationoutput-output.md)
```

## Properties<a name="aws-resource-kinesisanalyticsv2-applicationoutput-properties"></a>

`ApplicationName`  <a name="cfn-kinesisanalyticsv2-applicationoutput-applicationname"></a>
The name of your application \(for example, sample\-app\)\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Output`  <a name="cfn-kinesisanalyticsv2-applicationoutput-output"></a>
Describes an SQL\-based Kinesis Data Analytics application's output configuration\.  
 *Required*: Yes  
 *Type*: [Output](aws-properties-kinesisanalyticsv2-applicationoutput-output.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Examples<a name="aws-resource-kinesisanalyticsv2-applicationoutput-examples"></a>

### ApplicationOutput example<a name="aws-resource-kinesisanalyticsv2-applicationoutput-example1"></a>

The following example demonstrates how to create an `ApplicationOutput` object\.

#### YAML<a name="aws-resource-kinesisanalyticsv2-applicationoutput-example1.yaml"></a>

```
Type: AWS::KinesisAnalytics::ApplicationOutput
Properties:
  ApplicationName: !Ref BasicApplication
  Output:
    Name: "exampleOutput"
    DestinationSchema:
      RecordFormatType: "CSV"
    KinesisStreamsOutput:
      ResourceARN: !GetAtt OutputKinesisStream.Arn
```