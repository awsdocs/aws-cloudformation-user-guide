# AWS::IoTAnalytics::Datastore DatastorePartition<a name="aws-properties-iotanalytics-datastore-datastorepartition"></a>

A single dimension to partition a data store\. The dimension must be an `AttributePartition` or a `TimestampPartition`\.

## Syntax<a name="aws-properties-iotanalytics-datastore-datastorepartition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-datastore-datastorepartition-syntax.json"></a>

```
{
  "[Partition](#cfn-iotanalytics-datastore-datastorepartition-partition)" : Partition,
  "[TimestampPartition](#cfn-iotanalytics-datastore-datastorepartition-timestamppartition)" : TimestampPartition
}
```

### YAML<a name="aws-properties-iotanalytics-datastore-datastorepartition-syntax.yaml"></a>

```
  [Partition](#cfn-iotanalytics-datastore-datastorepartition-partition): 
    Partition
  [TimestampPartition](#cfn-iotanalytics-datastore-datastorepartition-timestamppartition): 
    TimestampPartition
```

## Properties<a name="aws-properties-iotanalytics-datastore-datastorepartition-properties"></a>

`Partition`  <a name="cfn-iotanalytics-datastore-datastorepartition-partition"></a>
A partition dimension defined by an attribute\.  
*Required*: No  
*Type*: [Partition](aws-properties-iotanalytics-datastore-partition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimestampPartition`  <a name="cfn-iotanalytics-datastore-datastorepartition-timestamppartition"></a>
A partition dimension defined by a timestamp attribute\.  
*Required*: No  
*Type*: [TimestampPartition](aws-properties-iotanalytics-datastore-timestamppartition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)