# Amazon Kinesis Data Analytics ApplicationReferenceDataSource ReferenceDataSource<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-description"></a>The `ReferenceDataSource` property type specifies the reference data source for a SQL\-based Amazon Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-inheritance"></a> `ReferenceDataSource` is a property of the [AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource](aws-resource-kinesisanalyticsv2-applicationreferencedatasource.md) resource\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-syntax.json"></a>

```
{
  "[ReferenceSchema](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-referenceschema)" : [*ReferenceSchema*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referenceschema.md),
  "[TableName](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-tablename)" : String,
  "[S3ReferenceDataSource](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-s3referencedatasource)" : [*S3ReferenceDataSource*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource.md)
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-syntax.yaml"></a>

```
[ReferenceSchema](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-referenceschema): [*ReferenceSchema*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referenceschema.md)
[TableName](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-tablename): String
[S3ReferenceDataSource](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-s3referencedatasource): [*S3ReferenceDataSource*](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource.md)
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-properties"></a>

`ReferenceSchema`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-referenceschema"></a>
Describes the format of the data in the streaming source, and how each data element maps to corresponding columns created in the in\-application stream\.   
 *Required*: Yes  
 *Type*: [ReferenceSchema](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referenceschema.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TableName`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-tablename"></a>
The name of the in\-application table to create\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`S3ReferenceDataSource`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource-s3referencedatasource"></a>
Identifies the S3 bucket and object that contains the reference data\.  
 *Required*: No  
 *Type*: [S3ReferenceDataSource](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-s3referencedatasource.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 