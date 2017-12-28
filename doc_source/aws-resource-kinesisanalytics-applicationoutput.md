# AWS::KinesisAnalytics::ApplicationOutput<a name="aws-resource-kinesisanalytics-applicationoutput"></a>

The `AWS::KinesisAnalytics::ApplicationOutput` resource adds an external destination to your Amazon Kinesis Data Analytics application\. For more information, see [AddApplicationOutput](http://docs.aws.amazon.com/kinesisanalytics/latest/dev/API_AddApplicationOutput.html) in the *Amazon Kinesis Data Analytics Developer Guide*\. 


+ [Syntax](#aws-resource-kinesisanalytics-applicationoutput-syntax)
+ [Properties](#aws-resource-kinesisanalytics-applicationoutput-properties)
+ [Examples](#aws-resource-kinesisanalytics-applicationoutput-examples)

## Syntax<a name="aws-resource-kinesisanalytics-applicationoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisanalytics-applicationoutput-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisAnalytics::ApplicationOutput",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-applicationname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-output)" : Output
  }
}
```

### YAML<a name="aws-resource-kinesisanalytics-applicationoutput-syntax.yaml"></a>

```
Type: "AWS::KinesisAnalytics::ApplicationOutput"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-applicationname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-applicationoutput-output): 
    Output
```

## Properties<a name="aws-resource-kinesisanalytics-applicationoutput-properties"></a>

`ApplicationName`  
The name of the application to which you want to add the output configuration\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: Replacement 

`Output`  
An array of objects, each describing one output configuration\.   
 *Required*: Yes  
 *Type*: [Kinesis Data Analytics ApplicationOutput Output](aws-properties-kinesisanalytics-applicationoutput-output.md)  
 *Update requires*: No interruption 

## Examples<a name="aws-resource-kinesisanalytics-applicationoutput-examples"></a>

### Adding an ApplicationOutput Resource<a name="aws-resource-kinesisanalytics-applicationoutput-examples-adding"></a>

The following example adds an `ApplicationOutput` resource to an Amazon Kinesis Data Analytics application\.

#### YAML<a name="aws-resource-kinesisanalytics-applicationoutput-example1.yaml"></a>

```
Type: "AWS::KinesisAnalytics::ApplicationOutput"
    Properties:
      ApplicationName: !Ref BasicApplication
      Output:
        Name: "exampleOutput"
        DestinationSchema:
          RecordFormatType: "CSV"
        KinesisStreamsOutput:
          ResourceARN: !GetAtt OutputKinesisStream.Arn
          RoleARN: !GetAtt KinesisAnalyticsRole.Arn
```