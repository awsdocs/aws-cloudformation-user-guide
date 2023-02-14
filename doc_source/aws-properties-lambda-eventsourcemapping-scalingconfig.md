# AWS::Lambda::EventSourceMapping ScalingConfig<a name="aws-properties-lambda-eventsourcemapping-scalingconfig"></a>

\(Amazon Simple Queue Service only\) The scaling configuration for the event source\. For more information, see [Configuring maximum concurrency for Amazon SQS event sources](https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html#events-sqs-max-concurrency)\.

## Syntax<a name="aws-properties-lambda-eventsourcemapping-scalingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-eventsourcemapping-scalingconfig-syntax.json"></a>

```
{
  "[MaximumConcurrency](#cfn-lambda-eventsourcemapping-scalingconfig-maximumconcurrency)" : Integer
}
```

### YAML<a name="aws-properties-lambda-eventsourcemapping-scalingconfig-syntax.yaml"></a>

```
  [MaximumConcurrency](#cfn-lambda-eventsourcemapping-scalingconfig-maximumconcurrency): Integer
```

## Properties<a name="aws-properties-lambda-eventsourcemapping-scalingconfig-properties"></a>

`MaximumConcurrency`  <a name="cfn-lambda-eventsourcemapping-scalingconfig-maximumconcurrency"></a>
Limits the number of concurrent instances that the Amazon SQS event source can invoke\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `2`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)