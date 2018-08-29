# AWS::KinesisAnalytics::ApplicationReferenceDataSource<a name="aws-resource-kinesisanalytics-applicationreferencedatasource"></a>

Use the AWS CloudFormation `AWS::KinesisAnalytics::ApplicationReferenceDataSource` resource to add a reference data source to an existing Amazon Kinesis Data Analytics application\. For more information, see `[AddApplicationReferenceDataSource](http://docs.aws.amazon.com/kinesisanalytics/latest/dev/API_AddApplicationReferenceDataSource.html)` in the *Amazon Kinesis Data Analytics Developer Guide*\. 

**Topics**
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
    "[ApplicationName](#cfn-kinesisanalytics-applicationreferencedatasource-applicationname)" : String,
    "[ReferenceDataSource](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource)" : [*ReferenceDataSource*](aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource.md),
  }
}
```

### YAML<a name="aws-resource-kinesisanalytics-applicationreferencedatasource-syntax.yaml"></a>

```
Type: "AWS::KinesisAnalytics::ApplicationReferenceDataSource"
Properties:
  [ApplicationName](#cfn-kinesisanalytics-applicationreferencedatasource-applicationname): String
  [ReferenceDataSource](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource): 
    [*ReferenceDataSource*](aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource.md)
```

## Properties<a name="aws-resource-kinesisanalytics-applicationreferencedatasource-properties"></a>

`ApplicationName`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-applicationname"></a>
The name of an existing application\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ReferenceDataSource`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource"></a>
The reference data source, which is an object in your Amazon Simple Storage Service \(Amazon S3\) bucket\.   
 *Required*: Yes  
 *Type*: [Kinesis Data Analytics ApplicationReferenceDataSource ReferenceDataSource](aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

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