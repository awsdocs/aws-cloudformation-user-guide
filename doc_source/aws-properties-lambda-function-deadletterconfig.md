# AWS::Lambda::Function DeadLetterConfig<a name="aws-properties-lambda-function-deadletterconfig"></a>

The [dead\-letter queue](https://docs.aws.amazon.com/lambda/latest/dg/invocation-async.html#dlq) for failed asynchronous invocations\.

## Syntax<a name="aws-properties-lambda-function-deadletterconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-function-deadletterconfig-syntax.json"></a>

```
{
  "[TargetArn](#cfn-lambda-function-deadletterconfig-targetarn)" : String
}
```

### YAML<a name="aws-properties-lambda-function-deadletterconfig-syntax.yaml"></a>

```
  [TargetArn](#cfn-lambda-function-deadletterconfig-targetarn): String
```

## Properties<a name="aws-properties-lambda-function-deadletterconfig-properties"></a>

`TargetArn`  <a name="cfn-lambda-function-deadletterconfig-targetarn"></a>
The Amazon Resource Name \(ARN\) of an Amazon SQS queue or Amazon SNS topic\.  
*Required*: No  
*Type*: String  
*Pattern*: `(arn:(aws[a-zA-Z-]*)?:[a-z0-9-.]+:.*)|()`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-lambda-function-deadletterconfig--examples"></a>

### Dead\-letter Queue<a name="aws-properties-lambda-function-deadletterconfig--examples--Dead-letter_Queue"></a>

Add a dead\-letter queue to a function\.

#### YAML<a name="aws-properties-lambda-function-deadletterconfig--examples--Dead-letter_Queue--yaml"></a>

```
      DeadLetterConfig:
        TargetArn: arn:aws:sqs:us-east-2:123456789012:dlq
```