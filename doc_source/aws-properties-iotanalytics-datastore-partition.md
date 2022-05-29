# AWS::IoTAnalytics::Datastore Partition<a name="aws-properties-iotanalytics-datastore-partition"></a>

A single dimension to partition a data store\. The dimension must be an `AttributePartition` or a `TimestampPartition`\.

## Syntax<a name="aws-properties-iotanalytics-datastore-partition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-datastore-partition-syntax.json"></a>

```
{
  "[AttributeName](#cfn-iotanalytics-datastore-partition-attributename)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-datastore-partition-syntax.yaml"></a>

```
  [AttributeName](#cfn-iotanalytics-datastore-partition-attributename): String
```

## Properties<a name="aws-properties-iotanalytics-datastore-partition-properties"></a>

`AttributeName`  <a name="cfn-iotanalytics-datastore-partition-attributename"></a>
The name of the attribute that defines a partition dimension\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)