# AWS::KinesisAnalytics::ApplicationReferenceDataSource<a name="aws-resource-kinesisanalytics-applicationreferencedatasource"></a>

Adds a reference data source to an existing application\.

Amazon Kinesis Analytics reads reference data \(that is, an Amazon S3 object\) and creates an in\-application table within your application\. In the request, you provide the source \(S3 bucket name and object key name\), name of the in\-application table to create, and the necessary mapping information that describes how data in Amazon S3 object maps to columns in the resulting in\-application table\.

 For conceptual information, see [Configuring Application Input](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/how-it-works-input.html)\. For the limits on data sources you can add to your application, see [Limits](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/limits.html)\. 

 This operation requires permissions to perform the `kinesisanalytics:AddApplicationOutput` action\. 

## Syntax<a name="aws-resource-kinesisanalytics-applicationreferencedatasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisanalytics-applicationreferencedatasource-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisAnalytics::ApplicationReferenceDataSource",
  "Properties" : {
      "[ApplicationName](#cfn-kinesisanalytics-applicationreferencedatasource-applicationname)" : String,
      "[ReferenceDataSource](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource)" : ReferenceDataSource
    }
}
```

### YAML<a name="aws-resource-kinesisanalytics-applicationreferencedatasource-syntax.yaml"></a>

```
Type: AWS::KinesisAnalytics::ApplicationReferenceDataSource
Properties: 
  [ApplicationName](#cfn-kinesisanalytics-applicationreferencedatasource-applicationname): String
  [ReferenceDataSource](#cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource): 
    ReferenceDataSource
```

## Properties<a name="aws-resource-kinesisanalytics-applicationreferencedatasource-properties"></a>

`ApplicationName`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-applicationname"></a>
Name of an existing application\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReferenceDataSource`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-referencedatasource"></a>
The reference data source can be an object in your Amazon S3 bucket\. Amazon Kinesis Analytics reads the object and copies the data into the in\-application table that is created\. You provide an S3 bucket, object key name, and the resulting in\-application table that is created\. You must also provide an IAM role with the necessary permissions that Amazon Kinesis Analytics can assume to read the object from your S3 bucket on your behalf\.  
*Required*: Yes  
*Type*: [ReferenceDataSource](aws-properties-kinesisanalytics-applicationreferencedatasource-referencedatasource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-kinesisanalytics-applicationreferencedatasource--examples"></a>



### Adding an ApplicationReferenceDataSource Resource<a name="aws-resource-kinesisanalytics-applicationreferencedatasource--examples--Adding_an_ApplicationReferenceDataSource_Resource"></a>

The following example creates an `ApplicationReferenceDataSource` resource: 

#### YAML<a name="aws-resource-kinesisanalytics-applicationreferencedatasource--examples--Adding_an_ApplicationReferenceDataSource_Resource--yaml"></a>

```
ApplicationReferenceDataSource:
    Type: AWS::KinesisAnalytics::ApplicationReferenceDataSource
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