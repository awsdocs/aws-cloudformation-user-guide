# AWS::KinesisAnalytics::Application<a name="aws-resource-kinesisanalytics-application"></a>

The `AWS::KinesisAnalytics::Application` resource creates an Amazon Kinesis Data Analytics application\. For more information, see the [http://docs.aws.amazon.com/kinesisanalytics/latest/dev/](http://docs.aws.amazon.com/kinesisanalytics/latest/dev/)\. 

## Syntax<a name="aws-resource-kinesisanalytics-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisanalytics-application-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisAnalytics::Application",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-applicationname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-applicationdescription)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-applicationcode)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-inputs)" : [ Input, ... ]
  }
}
```

### YAML<a name="aws-resource-kinesisanalytics-application-syntax.yaml"></a>

```
Type: "AWS::KinesisAnalytics::Application"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-applicationname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-applicationdescription): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-applicationcode): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-inputs): 
    - Input
```

## Properties<a name="aws-resource-kinesisanalytics-application-properties"></a>

`ApplicationName`  
The name of your Amazon Kinesis Data Analytics application\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

`ApplicationDescription`  
The summary description of the application\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`ApplicationCode`  
One or more SQL statements that read input data, transform it, and generate output\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Inputs`  
Use this parameter to configure the application input\.  
 *Required*: Yes  
 *Type*: List of [Kinesis Data Analytics Application Input](aws-properties-kinesisanalytics-application-input.md)  
 *Update requires*: No interruption 

## Example<a name="aws-resource-kinesisanalytics-application-examples"></a>

### Creating an Amazon Kinesis Data Analytics Application<a name="aws-resource-kinesisanalytics-application-examples-creating"></a>

The following example demonstrates how to create and configure a Kinesis Data Analytics application\.

#### YAML<a name="aws-resource-kinesisanalytics-application-example1.yaml"></a>

```
---
Description: "Sample KinesisAnalytics via CloudFormation"
Resources:
  BasicApplication:
    Type: "AWS::KinesisAnalytics::Application"
    Properties:
      ApplicationName: "sampleApplication"
      ApplicationDescription: "SampleApp"
      ApplicationCode: "Example Application Code"
      Inputs:
        - NamePrefix: "exampleNamePrefix"
          InputSchema:
            RecordColumns:
             - Name: "example"
               SqlType: "VARCHAR(16)"
               Mapping: "$.example"
            RecordFormat:
              RecordFormatType: "JSON"
              MappingParameters:
                JSONMappingParameters:
                  RecordRowPath: "$"
          KinesisStreamsInput:
            ResourceARN: !GetAtt InputKinesisStream.Arn
            RoleARN: !GetAtt KinesisAnalyticsRole.Arn
  InputKinesisStream:
    Type: "AWS::Kinesis::Stream"
    Properties:
      ShardCount: 1
  KinesisAnalyticsRole:
    Type: "AWS::IAM::Role"
    Properties:
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          - Effect: Allow
            Principal:
              Service: kinesisanalytics.amazonaws.com
            Action: "sts:AssumeRole"
      Path: "/"
      Policies:
        - PolicyName: Open
          PolicyDocument:
            Version: "2012-10-17"
            Statement:
              - Effect: Allow
                Action: "*"
                Resource: "*"
  BasicApplicationOutputs:
    Type: "AWS::KinesisAnalytics::ApplicationOutput"
    DependsOn: BasicApplication
    Properties:
      ApplicationName: !Ref BasicApplication
      Output:
        Name: "exampleOutput"
        DestinationSchema:
          RecordFormatType: "CSV"
        KinesisStreamsOutput:
          ResourceARN: !GetAtt OutputKinesisStream.Arn
          RoleARN: !GetAtt KinesisAnalyticsRole.Arn
  OutputKinesisStream:
    Type: "AWS::Kinesis::Stream"
    Properties:
      ShardCount: 1
  ApplicationReferenceDataSource:
    Type: "AWS::KinesisAnalytics::ApplicationReferenceDataSource"
    DependsOn: BasicApplicationOutputs
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
  S3Bucket:
    Type: AWS::S3::Bucket
Outputs:
  ApplicationPhysicalResourceId:
    Value: !Ref BasicApplication
```