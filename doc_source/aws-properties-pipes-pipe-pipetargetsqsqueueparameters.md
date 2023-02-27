# AWS::Pipes::Pipe PipeTargetSqsQueueParameters<a name="aws-properties-pipes-pipe-pipetargetsqsqueueparameters"></a>

The parameters for using a Amazon SQS stream as a source\.

## Syntax<a name="aws-properties-pipes-pipe-pipetargetsqsqueueparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipetargetsqsqueueparameters-syntax.json"></a>

```
{
  "[MessageDeduplicationId](#cfn-pipes-pipe-pipetargetsqsqueueparameters-messagededuplicationid)" : String,
  "[MessageGroupId](#cfn-pipes-pipe-pipetargetsqsqueueparameters-messagegroupid)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-pipetargetsqsqueueparameters-syntax.yaml"></a>

```
  [MessageDeduplicationId](#cfn-pipes-pipe-pipetargetsqsqueueparameters-messagededuplicationid): String
  [MessageGroupId](#cfn-pipes-pipe-pipetargetsqsqueueparameters-messagegroupid): String
```

## Properties<a name="aws-properties-pipes-pipe-pipetargetsqsqueueparameters-properties"></a>

`MessageDeduplicationId`  <a name="cfn-pipes-pipe-pipetargetsqsqueueparameters-messagededuplicationid"></a>
This parameter applies only to FIFO \(first\-in\-first\-out\) queues\.  
The token used for deduplication of sent messages\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageGroupId`  <a name="cfn-pipes-pipe-pipetargetsqsqueueparameters-messagegroupid"></a>
The FIFO message group ID to use as the target\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)