# AWS::KinesisAnalyticsV2::Application<a name="aws-resource-kinesisanalyticsv2-application"></a>

The `AWS::KinesisAnalyticsV2::Application` resource creates an Amazon Kinesis Data Analytics application\. For more information, see the [https://docs.aws.amazon.com/kinesisanalytics/latest/java/what-is.html](https://docs.aws.amazon.com/kinesisanalytics/latest/java/what-is.html)\. 

## Syntax<a name="aws-resource-kinesisanalyticsv2-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisanalyticsv2-application-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisAnalyticsV2::Application",
  "Properties" : {
    "[ApplicationName](#cfn-kinesisanalyticsv2-application-applicationname)" : String,
    "[RuntimeEnvironment](#cfn-kinesisanalyticsv2-application-runtimeenvironment)" : String,
    "[ApplicationConfiguration](#cfn-kinesisanalyticsv2-application-applicationconfiguration)" : [*ApplicationConfiguration*](aws-properties-kinesisanalyticsv2-application-applicationconfiguration.md),
    "[ApplicationDescription](#cfn-kinesisanalyticsv2-application-applicationdescription)" : String,
    "[ServiceExecutionRole](#cfn-kinesisanalyticsv2-application-serviceexecutionrole)" : String
  }
}
```

### YAML<a name="aws-resource-kinesisanalyticsv2-application-syntax.yaml"></a>

```
Type: "AWS::KinesisAnalyticsV2::Application"
Properties:
  [ApplicationName](#cfn-kinesisanalyticsv2-application-applicationname): String
  [RuntimeEnvironment](#cfn-kinesisanalyticsv2-application-runtimeenvironment): String
  [ApplicationConfiguration](#cfn-kinesisanalyticsv2-application-applicationconfiguration): [*ApplicationConfiguration*](aws-properties-kinesisanalyticsv2-application-applicationconfiguration.md)
  [ApplicationDescription](#cfn-kinesisanalyticsv2-application-applicationdescription): String
  [ServiceExecutionRole](#cfn-kinesisanalyticsv2-application-serviceexecutionrole): String
```

## Properties<a name="aws-resource-kinesisanalyticsv2-application-properties"></a>

`ApplicationName`  <a name="cfn-kinesisanalyticsv2-application-applicationname"></a>
The name of your Amazon Kinesis Analytics application \(for example, sample\-app\)\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`RuntimeEnvironment`  <a name="cfn-kinesisanalyticsv2-application-runtimeenvironment"></a>
The runtime environment for the application \(SQL\-1\.0 or FLINK\-1\_6\)\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ApplicationConfiguration`  <a name="cfn-kinesisanalyticsv2-application-applicationconfiguration"></a>
Use this parameter to configure the application\.  
 *Required*: No  
 *Type*: [ApplicationConfiguration](aws-properties-kinesisanalyticsv2-application-applicationconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ApplicationDescription`  <a name="cfn-kinesisanalyticsv2-application-applicationdescription"></a>
A summary description of the application\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ServiceExecutionRole`  <a name="cfn-kinesisanalyticsv2-application-serviceexecutionrole"></a>
The IAM role used by the application to access Kinesis data streams, Kinesis Data Firehose delivery streams, Amazon S3 objects, and other external resources\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Examples<a name="aws-resource-kinesisanalyticsv2-application-examples"></a>

### Application Example<a name="aws-resource-kinesisanalyticsv2-application-example1"></a>

The following example creates an `Application` resource\.

#### YAML<a name="aws-resource-kinesisanalyticsv2-application-example1.yaml"></a>

```
Description: "Sample KinesisAnalytics via CloudFormation"
Resources:
  BasicApplication:
    Type: AWS::KinesisAnalyticsV2::Application
    Properties:
      ApplicationName: "sampleApplication"
      ApplicationDescription: "SampleApp"
      RuntimeEnvironment: "SQL-1_0"
      ServiceExecutionRole: !GetAtt ServiceExecutionRole.Arn
      ApplicationConfiguration:
        SqlApplicationConfiguration:
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
                ResourceARN: !GetAtt SQLCanaryInputStream.Arn
        ApplicationCodeConfiguration:
          CodeContent:
            TextContent: "Example Application Code"
          CodeContentType: "PLAINTEXT"
  ServiceExecutionRole:
    Type: "AWS::IAM::Role"
    Properties:
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          - Effect: "Allow"
            Principal:
              Service: "kinesisanalytics.amazonaws.com"
            Action: "sts:AssumeRole"
      Path: "/"
      Policies:
        - PolicyName: "Open"
          PolicyDocument:
            Version: "2012-10-17"
            Statement:
              - Effect: "Allow"
                Action: "*"
                Resource: "*"
  InputKinesisStream:
    Type: AWS::Kinesis::Stream
    Properties:
      ShardCount: 1
  KinesisAnalyticsRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          - Effect: Allow
            Principal:
              Service: "kinesisanalytics.amazonaws.com"
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
    Type: AWS::KinesisAnalytics::ApplicationOutput
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
    Type: AWS::Kinesis::Stream
    Properties:
      ShardCount: 1
  BasicApplicationReferenceDataSource:
    Type: AWS::KinesisAnalytics::ApplicationReferenceDataSource
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
          FileKey: "fakeKey"
          ReferenceRoleARN: !GetAtt KinesisAnalyticsRole.Arn
  S3Bucket:
    Type: AWS::S3::Bucket
Outputs:
  ApplicationPhysicalResourceId:
    Value: !Ref BasicApplication
```