# AWS::IoTAnalytics::Pipeline Lambda<a name="aws-properties-iotanalytics-pipeline-lambda"></a>

An activity that runs a Lambda function to modify the message\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-lambda-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-lambda-syntax.json"></a>

```
{
  "[BatchSize](#cfn-iotanalytics-pipeline-lambda-batchsize)" : Integer,
  "[LambdaName](#cfn-iotanalytics-pipeline-lambda-lambdaname)" : String,
  "[Name](#cfn-iotanalytics-pipeline-lambda-name)" : String,
  "[Next](#cfn-iotanalytics-pipeline-lambda-next)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-lambda-syntax.yaml"></a>

```
  [BatchSize](#cfn-iotanalytics-pipeline-lambda-batchsize): Integer
  [LambdaName](#cfn-iotanalytics-pipeline-lambda-lambdaname): String
  [Name](#cfn-iotanalytics-pipeline-lambda-name): String
  [Next](#cfn-iotanalytics-pipeline-lambda-next): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-lambda-properties"></a>

`BatchSize`  <a name="cfn-iotanalytics-pipeline-lambda-batchsize"></a>
The number of messages passed to the Lambda function for processing\.  
The AWS Lambda function must be able to process all of these messages within five minutes, which is the maximum timeout duration for Lambda functions\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaName`  <a name="cfn-iotanalytics-pipeline-lambda-lambdaname"></a>
The name of the Lambda function that is run on the message\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `^[a-zA-Z0-9_-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotanalytics-pipeline-lambda-name"></a>
The name of the 'lambda' activity\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Next`  <a name="cfn-iotanalytics-pipeline-lambda-next"></a>
The next activity in the pipeline\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)