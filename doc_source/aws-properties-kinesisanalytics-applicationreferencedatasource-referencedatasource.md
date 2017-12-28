# Amazon Kinesis Data Analytics ApplicationReferenceDataSource ReferenceDataSource<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource"></a>

The `ReferenceDataSource` property type specifies the reference data source by providing the source information \(Amazon S3 bucket name and object key name\), the resulting in\-application table name that is created, and the necessary schema to map the data elements in the Amazon S3 object to the in\-application table\. 

 `ReferenceDataSource` is a property of the [AWS::KinesisAnalytics::ApplicationReferenceDataSource](aws-resource-kinesisanalytics-applicationreferencedatasource.md) resource\. 

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-tablename)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-s3referencedatasource)" : S3ReferenceDataSource,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-referenceschema)" : ReferenceSchema
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-tablename): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-s3referencedatasource): 
    S3ReferenceDataSource
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-referenceschema): 
    ReferenceSchema
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource-properties"></a>

`TableName`  
The name of the in\-application table to create\.  
 *Required*: No  
 *Type*: String;  
 *Update requires*: No interruption 

`S3ReferenceDataSource`  
Identifies the Amazon S3 bucket and object that contains the reference data\. Also identifies the IAM role that Amazon Kinesis Data Analytics can assume to read this object on your behalf\.   
 *Required*: No  
 *Type*: [Kinesis Data Analytics ApplicationReferenceDataSource S3ReferenceDataSource](aws-properties-kinesisanalytics-applicationreferencedatasource-s3referencedatasource.md)  
 *Update requires*: No interruption 

`ReferenceSchema`  
Describes the format of the data in the streaming source, and how each data element maps to corresponding columns that are created in the in\-application stream\.   
 *Required*: Yes  
 *Type*: [Kinesis Data Analytics ApplicationReferenceDataSource ReferenceSchema](aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema.md)  
 *Update requires*: No interruption 