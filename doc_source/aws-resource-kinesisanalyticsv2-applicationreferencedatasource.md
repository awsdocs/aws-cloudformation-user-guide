# AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource"></a>

Adds a reference data source to an existing SQL\-based Kinesis Data Analytics application\.

Kinesis Data Analytics reads reference data \(that is, an Amazon S3 object\) and creates an in\-application table within your application\. In the request, you provide the source \(S3 bucket name and object key name\), name of the in\-application table to create, and the necessary mapping information that describes how data in an Amazon S3 object maps to columns in the resulting in\-application table\.

## Syntax<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource",
  "Properties" : {
      "[ApplicationName](#cfn-kinesisanalyticsv2-applicationreferencedatasource-applicationname)" : String,
      "[ReferenceDataSource](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource)" : ReferenceDataSource
    }
}
```

### YAML<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource-syntax.yaml"></a>

```
Type: AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource
Properties: 
  [ApplicationName](#cfn-kinesisanalyticsv2-applicationreferencedatasource-applicationname): String
  [ReferenceDataSource](#cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource): 
    ReferenceDataSource
```

## Properties<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource-properties"></a>

`ApplicationName`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-applicationname"></a>
The name of the application\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReferenceDataSource`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource"></a>
For a SQL\-based Kinesis Data Analytics application, describes the reference data source by providing the source information \(Amazon S3 bucket name and object key name\), the resulting in\-application table name that is created, and the necessary schema to map the data elements in the Amazon S3 object to the in\-application table\.  
*Required*: Yes  
*Type*: [ReferenceDataSource](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-referencedatasource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource--examples"></a>



### Create an ApplicationReferenceDataSource resource<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource--examples--Create_an_ApplicationReferenceDataSource_resource"></a>

#### JSON<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource--examples--Create_an_ApplicationReferenceDataSource_resource--json"></a>

```
{
    "ApplicationReferenceDataSource": {
        "Type": "AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource",
        "Properties": {
            "ApplicationName": {
                "Ref": "BasicApplication"
            },
            "ReferenceDataSource": {
                "TableName": "exampleTable",
                "ReferenceSchema": {
                    "RecordColumns": [
                        {
                            "Name": "example",
                            "SqlType": "VARCHAR(16)",
                            "Mapping": "$.example"
                        }
                    ],
                    "RecordFormat": {
                        "RecordFormatType": "JSON",
                        "MappingParameters": {
                            "JSONMappingParameters": {
                                "RecordRowPath": "$"
                            }
                        }
                    }
                },
                "S3ReferenceDataSource": {
                    "BucketARN": {
                        "Fn::GetAtt": [
                            "S3Bucket",
                            "Arn"
                        ]
                    },
                    "FileKey": "fakeKey"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource--examples--Create_an_ApplicationReferenceDataSource_resource--yaml"></a>

```
ApplicationReferenceDataSource:
  Type: 'AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource'
  Properties:
    ApplicationName: !Ref BasicApplication
    ReferenceDataSource:
      TableName: exampleTable
      ReferenceSchema:
        RecordColumns:
          - Name: example
            SqlType: VARCHAR(16)
            Mapping: $.example
        RecordFormat:
          RecordFormatType: JSON
          MappingParameters:
            JSONMappingParameters:
              RecordRowPath: $
      S3ReferenceDataSource:
        BucketARN: !GetAtt 
          - S3Bucket
          - Arn
        FileKey: fakeKey
```

## See also<a name="aws-resource-kinesisanalyticsv2-applicationreferencedatasource--seealso"></a>
+  [AddApplicationReferenceDataSource](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_AddApplicationReferenceDataSource.html) in the *Amazon Kinesis Data Analytics API Reference* 

