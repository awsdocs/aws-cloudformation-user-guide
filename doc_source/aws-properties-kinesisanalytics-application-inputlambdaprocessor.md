# Amazon Kinesis Data Analytics Application InputLambdaProcessor<a name="aws-properties-kinesisanalytics-application-inputlambdaprocessor"></a>

The `InputLambdaProcessor` property type specifies the Amazon Resource Name \(ARN\) of a Lambda function for preprocessing records in a stream before the SQL code for an Amazon Kinesis Data Analytics application executes\. 

 `InputLambdaProcessor` is a property of the [Kinesis Data Analytics Application Input](aws-properties-kinesisanalytics-application-input.md) property type\. 

## Syntax<a name="aws-properties-kinesisanalytics-application-inputlambdaprocessor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-inputlambdaprocessor-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-inputlambdaprocessor-resourcearn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-inputlambdaprocessor-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-inputlambdaprocessor-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-inputlambdaprocessor-resourcearn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisanalytics-application-inputlambdaprocessor-rolearn): String
```

## Properties<a name="aws-properties-kinesisanalytics-application-inputlambdaprocessor-properties"></a>

`ResourceARN`  
The ARN of the AWS Lambda function that operates on records in the stream\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`RoleARN`  
The ARN of the IAM role that is used to access the AWS Lambda function\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 