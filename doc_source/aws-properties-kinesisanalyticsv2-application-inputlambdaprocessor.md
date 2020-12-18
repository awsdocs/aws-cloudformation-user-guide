# AWS::KinesisAnalyticsV2::Application InputLambdaProcessor<a name="aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor"></a>

An object that contains the Amazon Resource Name \(ARN\) of the AWS Lambda function that is used to preprocess records in the stream in a SQL\-based Kinesis Data Analytics application\. 

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor-syntax.json"></a>

```
{
  "[ResourceARN](#cfn-kinesisanalyticsv2-application-inputlambdaprocessor-resourcearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor-syntax.yaml"></a>

```
  [ResourceARN](#cfn-kinesisanalyticsv2-application-inputlambdaprocessor-resourcearn): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor-properties"></a>

`ResourceARN`  <a name="cfn-kinesisanalyticsv2-application-inputlambdaprocessor-resourcearn"></a>
The ARN of the AWS Lambda function that operates on records in the stream\.  
To specify an earlier version of the Lambda function than the latest, include the Lambda function version in the Lambda function ARN\. For more information about Lambda ARNs, see [Example ARNs: AWS Lambda](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html#arn-syntax-lambda) 
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-inputlambdaprocessor--seealso"></a>
+  [InputLambdaProcessor](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_InputLambdaProcessor.html) in the *Amazon Kinesis Data Analytics API Reference* 

