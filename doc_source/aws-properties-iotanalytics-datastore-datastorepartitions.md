# AWS::IoTAnalytics::Datastore DatastorePartitions<a name="aws-properties-iotanalytics-datastore-datastorepartitions"></a>

Information about the partition dimensions in a data store\.

## Syntax<a name="aws-properties-iotanalytics-datastore-datastorepartitions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-datastore-datastorepartitions-syntax.json"></a>

```
{
  "[Partitions](#cfn-iotanalytics-datastore-datastorepartitions-partitions)" : [ DatastorePartition, ... ]
}
```

### YAML<a name="aws-properties-iotanalytics-datastore-datastorepartitions-syntax.yaml"></a>

```
  [Partitions](#cfn-iotanalytics-datastore-datastorepartitions-partitions): 
    - DatastorePartition
```

## Properties<a name="aws-properties-iotanalytics-datastore-datastorepartitions-properties"></a>

`Partitions`  <a name="cfn-iotanalytics-datastore-datastorepartitions-partitions"></a>
A list of partition dimensions in a data store\.   
*Required*: No  
*Type*: List of [DatastorePartition](aws-properties-iotanalytics-datastore-datastorepartition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)