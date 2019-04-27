# AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource"></a>

The `AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource` resource describes a reference data source for a SQL\-based Amazon Kinesis Data Analytics application\. 

## Syntax<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource",
  "Properties" : {
    "[ApplicationName](#cfn-kinesisanalyticsv2-applicationreferencedatasource-applicationname)" : String,
    "[ReferenceDataSource](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource)" : [*ReferenceDataSource*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource.md)
  }
}
```

### YAML<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource-syntax.yaml"></a>

```
Type: "AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource"
Properties:
  [ApplicationName](#cfn-kinesisanalyticsv2-applicationreferencedatasource-applicationname): String
  [ReferenceDataSource](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource): [*ReferenceDataSource*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource.md)
```

## Properties<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource-properties"></a>

`ApplicationName`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-applicationname"></a>
The application name\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ReferenceDataSource`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource"></a>
For an SQL\-based Amazon Kinesis Data Analytics application, describes the reference data source\.  
 *Required*: Yes  
 *Type*: [ReferenceDataSource](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Examples<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource-examples"></a>

### ApplicationReferenceDataSource<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource-example1"></a>

The following example creates an `ApplicationReferenceDataSource` resource\.

#### YAML<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource-example1.yaml"></a>

```
ApplicationReferenceDataSource:
  Type: AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource
  Properties:
    ApplicationName: !Ref BasicApplication
    ReferenceDataSource:
      TableName: "exampleTable"
      ReferenceSchema:
        RecordColumns:
          - Name: "example"
            SqlType: "VARCHAR(16)"
            Mapping: "$.example"
        RecordFormat:
          RecordFormatType: "JSON"
          MappingParameters:
            JSONMappingParameters:
              RecordRowPath: "$"
      S3ReferenceDataSource:
        BucketARN: !GetAtt S3Bucket.Arn
        FileKey: 'fakeKey'
```