# AWS::Pipes::Pipe PipeTargetKinesisStreamParameters<a name="aws-properties-pipes-pipe-pipetargetkinesisstreamparameters"></a>

The parameters for using a Kinesis stream as a source\.

## Syntax<a name="aws-properties-pipes-pipe-pipetargetkinesisstreamparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipetargetkinesisstreamparameters-syntax.json"></a>

```
{
  "[PartitionKey](#cfn-pipes-pipe-pipetargetkinesisstreamparameters-partitionkey)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-pipetargetkinesisstreamparameters-syntax.yaml"></a>

```
  [PartitionKey](#cfn-pipes-pipe-pipetargetkinesisstreamparameters-partitionkey): String
```

## Properties<a name="aws-properties-pipes-pipe-pipetargetkinesisstreamparameters-properties"></a>

`PartitionKey`  <a name="cfn-pipes-pipe-pipetargetkinesisstreamparameters-partitionkey"></a>
Determines which shard in the stream the data record is assigned to\. Partition keys are Unicode strings with a maximum length limit of 256 characters for each key\. Amazon Kinesis Data Streams uses the partition key as input to a hash function that maps the partition key and associated data to a specific shard\. Specifically, an MD5 hash function is used to map partition keys to 128\-bit integer values and to map associated data records to shards\. As a result of this hashing mechanism, all data records with the same partition key map to the same shard within the stream\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)