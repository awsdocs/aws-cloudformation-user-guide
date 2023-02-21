# AWS::Pipes::Pipe PipeSourceKinesisStreamParameters<a name="aws-properties-pipes-pipe-pipesourcekinesisstreamparameters"></a>

The parameters for using a Kinesis stream as a source\.

## Syntax<a name="aws-properties-pipes-pipe-pipesourcekinesisstreamparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipesourcekinesisstreamparameters-syntax.json"></a>

```
{
  "[BatchSize](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-batchsize)" : Integer,
  "[DeadLetterConfig](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-deadletterconfig)" : DeadLetterConfig,
  "[MaximumBatchingWindowInSeconds](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-maximumbatchingwindowinseconds)" : Integer,
  "[MaximumRecordAgeInSeconds](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-maximumrecordageinseconds)" : Integer,
  "[MaximumRetryAttempts](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-maximumretryattempts)" : Integer,
  "[OnPartialBatchItemFailure](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-onpartialbatchitemfailure)" : String,
  "[ParallelizationFactor](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-parallelizationfactor)" : Integer,
  "[StartingPosition](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-startingposition)" : String,
  "[StartingPositionTimestamp](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-startingpositiontimestamp)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-pipesourcekinesisstreamparameters-syntax.yaml"></a>

```
  [BatchSize](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-batchsize): Integer
  [DeadLetterConfig](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-deadletterconfig): 
    DeadLetterConfig
  [MaximumBatchingWindowInSeconds](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-maximumbatchingwindowinseconds): Integer
  [MaximumRecordAgeInSeconds](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-maximumrecordageinseconds): Integer
  [MaximumRetryAttempts](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-maximumretryattempts): Integer
  [OnPartialBatchItemFailure](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-onpartialbatchitemfailure): String
  [ParallelizationFactor](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-parallelizationfactor): Integer
  [StartingPosition](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-startingposition): String
  [StartingPositionTimestamp](#cfn-pipes-pipe-pipesourcekinesisstreamparameters-startingpositiontimestamp): String
```

## Properties<a name="aws-properties-pipes-pipe-pipesourcekinesisstreamparameters-properties"></a>

`BatchSize`  <a name="cfn-pipes-pipe-pipesourcekinesisstreamparameters-batchsize"></a>
The maximum number of records to include in each batch\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeadLetterConfig`  <a name="cfn-pipes-pipe-pipesourcekinesisstreamparameters-deadletterconfig"></a>
Define the target queue to send dead\-letter queue events to\.  
*Required*: No  
*Type*: [DeadLetterConfig](aws-properties-pipes-pipe-deadletterconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumBatchingWindowInSeconds`  <a name="cfn-pipes-pipe-pipesourcekinesisstreamparameters-maximumbatchingwindowinseconds"></a>
The maximum length of a time to wait for events\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumRecordAgeInSeconds`  <a name="cfn-pipes-pipe-pipesourcekinesisstreamparameters-maximumrecordageinseconds"></a>
\(Streams only\) Discard records older than the specified age\. The default value is \-1, which sets the maximum age to infinite\. When the value is set to infinite, EventBridge never discards old records\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumRetryAttempts`  <a name="cfn-pipes-pipe-pipesourcekinesisstreamparameters-maximumretryattempts"></a>
\(Streams only\) Discard records after the specified number of retries\. The default value is \-1, which sets the maximum number of retries to infinite\. When MaximumRetryAttempts is infinite, EventBridge retries failed records until the record expires in the event source\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnPartialBatchItemFailure`  <a name="cfn-pipes-pipe-pipesourcekinesisstreamparameters-onpartialbatchitemfailure"></a>
\(Streams only\) Define how to handle item process failures\. `AUTOMATIC_BISECT` halves each batch and retry each half until all the records are processed or there is one failed message left in the batch\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParallelizationFactor`  <a name="cfn-pipes-pipe-pipesourcekinesisstreamparameters-parallelizationfactor"></a>
\(Streams only\) The number of batches to process concurrently from each shard\. The default value is 1\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartingPosition`  <a name="cfn-pipes-pipe-pipesourcekinesisstreamparameters-startingposition"></a>
\(Streams only\) The position in a stream from which to start reading\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StartingPositionTimestamp`  <a name="cfn-pipes-pipe-pipesourcekinesisstreamparameters-startingpositiontimestamp"></a>
With `StartingPosition` set to `AT_TIMESTAMP`, the time from which to start reading, in Unix time seconds\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)