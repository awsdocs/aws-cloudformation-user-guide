# AWS::Events::Rule SqsParameters<a name="aws-properties-events-rule-sqsparameters"></a>

This structure includes the custom parameter to be used when the target is an SQS FIFO queue\.

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

`MessageGroupId`  <a name="cfn-events-rule-sqsparameters-messagegroupid"></a>
The FIFO message group ID to use as the target\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)