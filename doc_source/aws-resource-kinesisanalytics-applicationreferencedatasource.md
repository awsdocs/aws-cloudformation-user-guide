# AWS::KinesisAnalytics::ApplicationReferenceDataSource<a name="aws-resource-kinesisanalytics-applicationreferencedatasource"></a>

Use the AWS CloudFormation `AWS::KinesisAnalytics::ApplicationReferenceDataSource` resource to add a reference data source to an existing Amazon Kinesis Data Analytics application\. For more information, see `[AddApplicationReferenceDataSource](http://docs.aws.amazon.com/kinesisanalytics/latest/dev/API_AddApplicationReferenceDataSource.html)` in the *Amazon Kinesis Data Analytics Developer Guide*\. 


+ [Syntax](#aws-resource-kinesisanalytics-applicationreferencedatasource-syntax)
+ [Properties](#aws-resource-kinesisanalytics-applicationreferencedatasource-properties)
+ [Examples](#aws-resource-kinesisanalytics-applicationreferencedatasource-examples)

## Syntax<a name="aws-resource-kinesisanalytics-applicationreferencedatasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisanalytics-applicationreferencedatasource-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisAnalytics::ApplicationReferenceDataSource",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-applicationname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource)" : ReferenceDataSource,
  }
}
```

### YAML<a name="aws-resource-kinesisanalytics-applicationreferencedatasource-syntax.yaml"></a>

```
Type: "AWS::KinesisAnalytics::ApplicationReferenceDataSource"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-applicationname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource): 
    ReferenceDataSource
```

## Properties<a name="aws-resource-kinesisanalytics-applicationreferencedatasource-properties"></a>

`ApplicationName`  
The name of an existing application\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: Replacement 

`ReferenceDataSource`  
The reference data source, which is an object in your Amazon Simple Storage Service \(Amazon S3\) bucket\.   
 *Required*: Yes  
 *Type*: [Kinesis Data Analytics ApplicationReferenceDataSource ReferenceDataSource](aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource.md)  
 *Update requires*: No interruption 

## Examples<a name="aws-resource-kinesisanalytics-applicationreferencedatasource-examples"></a>

### Creating an ApplicationReferenceDataSource Resource<a name="aws-resource-kinesisanalytics-applicationreferencedatasource-examples-create"></a>

The following example creates an `ApplicationReferenceDataSource` resource:

#### YAML<a name="aws-resource-kinesisanalytics-applicationreferencedatasource-example1.yaml"></a>

```
ApplicationReferenceDataSource:
    Type: "AWS::KinesisAnalytics::ApplicationReferenceDataSource"
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
          ReferenceRoleARN: !GetAtt KinesisAnalyticsRole.Arn
```