# AWS::KinesisAnalytics::ApplicationOutput<a name="aws-resource-kinesisanalytics-applicationoutput"></a>

Adds an external destination to your Amazon Kinesis Analytics application\.

If you want Amazon Kinesis Analytics to deliver data from an in\-application stream within your application to an external destination \(such as an Amazon Kinesis stream, an Amazon Kinesis Firehose delivery stream, or an AWS Lambda function\), you add the relevant configuration to your application using this operation\. You can configure one or more outputs for your application\. Each output configuration maps an in\-application stream and an external destination\.

 You can use one of the output configurations to deliver data from your in\-application error stream to an external destination so that you can analyze the errors\. For more information, see [Understanding Application Output \(Destination\)](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/how-it-works-output.html)\. 

 Any configuration update, including adding a streaming source using this operation, results in a new version of the application\. You can use the `DescribeApplication` operation to find the current application version\.

For the limits on the number of application inputs and outputs you can configure, see [Limits](https://docs.aws.amazon.com/kinesisanalytics/latest/dev/limits.html)\.

This operation requires permissions to perform the `kinesisanalytics:AddApplicationOutput` action\.

## Syntax<a name="aws-resource-kinesisanalytics-applicationoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisanalytics-applicationoutput-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisAnalytics::ApplicationOutput",
  "Properties" : {
      "[ApplicationName](#cfn-kinesisanalytics-applicationoutput-applicationname)" : String,
      "[Output](#cfn-kinesisanalytics-applicationoutput-output)" : Output
    }
}
```

### YAML<a name="aws-resource-kinesisanalytics-applicationoutput-syntax.yaml"></a>

```
Type: AWS::KinesisAnalytics::ApplicationOutput
Properties: 
  [ApplicationName](#cfn-kinesisanalytics-applicationoutput-applicationname): String
  [Output](#cfn-kinesisanalytics-applicationoutput-output): 
    Output
```

## Properties<a name="aws-resource-kinesisanalytics-applicationoutput-properties"></a>

`ApplicationName`  <a name="cfn-kinesisanalytics-applicationoutput-applicationname"></a>
Name of the application to which you want to add the output configuration\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Output`  <a name="cfn-kinesisanalytics-applicationoutput-output"></a>
An array of objects, each describing one output configuration\. In the output configuration, you specify the name of an in\-application stream, a destination \(that is, an Amazon Kinesis stream, an Amazon Kinesis Firehose delivery stream, or an AWS Lambda function\), and record the formation to use when writing to the destination\.  
*Required*: Yes  
*Type*: [Output](aws-properties-kinesisanalytics-applicationoutput-output.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-kinesisanalytics-applicationoutput--examples"></a>



### Adding an ApplicationOutput Resource<a name="aws-resource-kinesisanalytics-applicationoutput--examples--Adding_an_ApplicationOutput_Resource"></a>

The following example creates an `ApplicationOutput` resource: 

#### YAML<a name="aws-resource-kinesisanalytics-applicationoutput--examples--Adding_an_ApplicationOutput_Resource--yaml"></a>

```
Type: AWS::KinesisAnalytics::ApplicationOutput
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