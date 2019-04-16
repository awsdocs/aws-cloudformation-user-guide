# AWS IoT Analytics Pipeline Lambda<a name="aws-properties-iotanalytics-pipeline-lambda"></a>

<a name="aws-properties-iotanalytics-pipeline-lambda-description"></a>The `Lambda` property type specifies a Lambda function to run to modify a message for an AWS IoT Analytics pipeline\.

<a name="aws-properties-iotanalytics-pipeline-lambda-inheritance"></a> `Lambda` is a property of the [Activity](aws-properties-iotanalytics-pipeline-activity.md) property type\.

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
The number of messages that should be passed to the Lambda function for processing within 5 minutes\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LambdaName`  <a name="cfn-iotanalytics-pipeline-lambda-lambdaname"></a>
The name of the Lambda function that is run on the message\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-iotanalytics-pipeline-lambda-name"></a>
The name of the 'lambda' activity\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Next`  <a name="cfn-iotanalytics-pipeline-lambda-next"></a>
The next activity in the pipeline\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-pipeline-lambda-seealso"></a>
+ [CreatePipeline](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createpipeline) in the *IoT Analytics User Guide*