# AWS::KinesisAnalyticsV2::ApplicationOutput<a name="aws-resource-kinesisanalyticsv2-applicationoutput"></a>

Adds an external destination to your SQL\-based Amazon Kinesis Data Analytics application\.

If you want Kinesis Data Analytics to deliver data from an in\-application stream within your application to an external destination \(such as an Kinesis data stream, a Kinesis Data Firehose delivery stream, or an AWS Lambda function\), you add the relevant configuration to your application using this operation\. You can configure one or more outputs for your application\. Each output configuration maps an in\-application stream and an external destination\.

 You can use one of the output configurations to deliver data from your in\-application error stream to an external destination so that you can analyze the errors\. 

 Any configuration update, including adding a streaming source using this operation, results in a new version of the application\. You can use the [DescribeApplication](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_DescribeApplication.html) operation to find the current application version\.

## Syntax<a name="aws-resource-kinesisanalyticsv2-applicationoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisanalyticsv2-applicationoutput-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisAnalyticsV2::ApplicationOutput",
  "Properties" : {
      "[ApplicationName](#cfn-kinesisanalyticsv2-applicationoutput-applicationname)" : String,
      "[Output](#cfn-kinesisanalyticsv2-applicationoutput-output)" : Output
    }
}
```

### YAML<a name="aws-resource-kinesisanalyticsv2-applicationoutput-syntax.yaml"></a>

```
Type: AWS::KinesisAnalyticsV2::ApplicationOutput
Properties: 
  [ApplicationName](#cfn-kinesisanalyticsv2-applicationoutput-applicationname): String
  [Output](#cfn-kinesisanalyticsv2-applicationoutput-output): 
    Output
```

## Properties<a name="aws-resource-kinesisanalyticsv2-applicationoutput-properties"></a>

`ApplicationName`  <a name="cfn-kinesisanalyticsv2-applicationoutput-applicationname"></a>
The name of the application\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Output`  <a name="cfn-kinesisanalyticsv2-applicationoutput-output"></a>
 Describes a SQL\-based Kinesis Data Analytics application's output configuration, in which you identify an in\-application stream and a destination where you want the in\-application stream data to be written\. The destination can be a Kinesis data stream or a Kinesis Data Firehose delivery stream\.   
  
*Required*: Yes  
*Type*: [Output](aws-properties-kinesisanalyticsv2-applicationoutput-output.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-kinesisanalyticsv2-applicationoutput--examples"></a>



### Create an ApplicationOutput object<a name="aws-resource-kinesisanalyticsv2-applicationoutput--examples--Create_an_ApplicationOutput_object"></a>

#### JSON<a name="aws-resource-kinesisanalyticsv2-applicationoutput--examples--Create_an_ApplicationOutput_object--json"></a>

```
{
    "Type": "AWS::KinesisAnalyticsV2::ApplicationOutput",
    "Properties": {
        "ApplicationName": {
            "Ref": "BasicApplication"
        },
        "Output": {
            "Name": "exampleOutput",
            "DestinationSchema": {
                "RecordFormatType": "CSV"
            },
            "KinesisStreamsOutput": {
                "ResourceARN": {
                    "Fn::GetAtt": [
                        "OutputKinesisStream",
                        "Arn"
                    ]
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-kinesisanalyticsv2-applicationoutput--examples--Create_an_ApplicationOutput_object--yaml"></a>

```
Type: 'AWS::KinesisAnalyticsV2::ApplicationOutput'
Properties:
  ApplicationName: !Ref BasicApplication
  Output:
    Name: exampleOutput
    DestinationSchema:
      RecordFormatType: CSV
    KinesisStreamsOutput:
      ResourceARN: !GetAtt 
        - OutputKinesisStream
        - Arn
```

## See also<a name="aws-resource-kinesisanalyticsv2-applicationoutput--seealso"></a>
+  [AddApplicationOutput](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_AddApplicationOutput.html) in the *Amazon Kinesis Data Analytics API Reference* 

