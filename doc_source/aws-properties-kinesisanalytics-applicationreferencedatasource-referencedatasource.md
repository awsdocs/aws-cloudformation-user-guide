# AWS::KinesisAnalytics::ApplicationReferenceDataSource ReferenceDataSource<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource"></a>

Describes the reference data source by providing the source information \(S3 bucket name and object key name\), the resulting in\-application table name that is created, and the necessary schema to map the data elements in the Amazon S3 object to the in\-application table\.

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource-syntax.json"></a>

```
{
  "[ReferenceSchema](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-referenceschema)" : ReferenceSchema,
  "[S3ReferenceDataSource](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-s3referencedatasource)" : S3ReferenceDataSource,
  "[TableName](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-tablename)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource-syntax.yaml"></a>

```
  [ReferenceSchema](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-referenceschema): 
    ReferenceSchema
  [S3ReferenceDataSource](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-s3referencedatasource): 
    S3ReferenceDataSource
  [TableName](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-tablename): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource-properties"></a>

`ReferenceSchema`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-referenceschema"></a>
Describes the format of the data in the streaming source, and how each data element maps to corresponding columns created in the in\-application stream\.  
*Required*: Yes  
*Type*: [ReferenceSchema](aws-properties-kinesisanalytics-applicationreferencedatasource-referenceschema.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3ReferenceDataSource`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-s3referencedatasource"></a>
Identifies the S3 bucket and object that contains the reference data\. Also identifies the IAM role Amazon Kinesis Analytics can assume to read this object on your behalf\. An Amazon Kinesis Analytics application loads reference data only once\. If the data changes, you call the `UpdateApplication` operation to trigger reloading of data into your application\.   
*Required*: No  
*Type*: [S3ReferenceDataSource](aws-properties-kinesisanalytics-applicationreferencedatasource-s3referencedatasource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource-tablename"></a>
Name of the in\-application table to create\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)