# AWS::Events::Rule DeadLetterConfig<a name="aws-properties-events-rule-deadletterconfig"></a>

A `DeadLetterConfig` object that contains information about a dead\-letter queue configuration\.

## Syntax<a name="aws-properties-events-rule-deadletterconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-deadletterconfig-syntax.json"></a>

```
{
  "[Arn](#cfn-events-rule-deadletterconfig-arn)" : String
}
```

### YAML<a name="aws-properties-events-rule-deadletterconfig-syntax.yaml"></a>

```
  [Arn](#cfn-events-rule-deadletterconfig-arn): String
```

## Properties<a name="aws-properties-events-rule-deadletterconfig-properties"></a>

`Arn`  <a name="cfn-events-rule-deadletterconfig-arn"></a>
The ARN of the SQS queue specified as the target for the dead\-letter queue\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-events-rule-deadletterconfig--examples"></a>



### Set the DeadLetterConfig parameter<a name="aws-properties-events-rule-deadletterconfig--examples--Set_the_DeadLetterConfig_parameter"></a>

The following example sets the `DeadLetterConfig` parameter to set up arn:aws:sqs:us\-west\-2:081035103721:demoDLQ as a dead\-letter queue\.

#### JSON<a name="aws-properties-events-rule-deadletterconfig--examples--Set_the_DeadLetterConfig_parameter--json"></a>

```
"DeadLetterConfig": {
  "Arn": "arn:aws:sqs:us-west-2:081035103721:demoDLQ"
}
```

#### YAML<a name="aws-properties-events-rule-deadletterconfig--examples--Set_the_DeadLetterConfig_parameter--yaml"></a>

```
DeadLetterConfig:
  Arn: 'arn:aws:sqs:us-west-2:081035103721:demoDLQ'
```