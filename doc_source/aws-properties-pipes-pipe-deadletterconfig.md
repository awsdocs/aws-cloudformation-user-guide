# AWS::Pipes::Pipe DeadLetterConfig<a name="aws-properties-pipes-pipe-deadletterconfig"></a>

A `DeadLetterConfig` object that contains information about a dead\-letter queue configuration\.

## Syntax<a name="aws-properties-pipes-pipe-deadletterconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-deadletterconfig-syntax.json"></a>

```
{
  "[Arn](#cfn-pipes-pipe-deadletterconfig-arn)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-deadletterconfig-syntax.yaml"></a>

```
  [Arn](#cfn-pipes-pipe-deadletterconfig-arn): String
```

## Properties<a name="aws-properties-pipes-pipe-deadletterconfig-properties"></a>

`Arn`  <a name="cfn-pipes-pipe-deadletterconfig-arn"></a>
The ARN of the Amazon SQS queue specified as the target for the dead\-letter queue\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)