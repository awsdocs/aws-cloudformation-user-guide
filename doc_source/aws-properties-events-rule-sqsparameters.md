# Amazon CloudWatch Events Rule SqsParameters<a name="aws-properties-events-rule-sqsparameters"></a>

<a name="aws-properties-events-rule-sqsparameters-description"></a>The `SqsParameters` property type specify the custom parameter to be used when the target is an Amazon SQS FIFO queue\.

<a name="aws-properties-events-rule-sqsparameters-inheritance"></a> `SqsParameters` is a sub\-property of the [Target](aws-properties-events-rule-target.md) property type\.

## Syntax<a name="aws-properties-events-rule-sqsparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-sqsparameters-syntax.json"></a>

```
{
  "[MessageGroupId](#cfn-events-rule-sqsparameters-messagegroupid)" : String
}
```

### YAML<a name="aws-properties-events-rule-sqsparameters-syntax.yaml"></a>

```
[MessageGroupId](#cfn-events-rule-sqsparameters-messagegroupid): String
```

## Properties<a name="aws-properties-events-rule-sqsparameters-properties"></a>

For more information, including constraints, see [SqsParameters](https://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_SqsParameters.html) in the *Amazon CloudWatch Events API Reference*\.

`MessageGroupId`  <a name="cfn-events-rule-sqsparameters-messagegroupid"></a>
The FIFO message group ID to use as the target\.  
 *Required*: Yes  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)