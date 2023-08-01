# AWS::Timestream::Table PartitionKey<a name="aws-properties-timestream-table-partitionkey"></a>

 An attribute used in partitioning data in a table\. A dimension key partitions data using the values of the dimension specified by the dimension\-name as partition key, while a measure key partitions data using measure names \(values of the 'measure\_name' column\)\. 

## Syntax<a name="aws-properties-timestream-table-partitionkey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-timestream-table-partitionkey-syntax.json"></a>

```
{
  "[EnforcementInRecord](#cfn-timestream-table-partitionkey-enforcementinrecord)" : String,
  "[Name](#cfn-timestream-table-partitionkey-name)" : String,
  "[Type](#cfn-timestream-table-partitionkey-type)" : String
}
```

### YAML<a name="aws-properties-timestream-table-partitionkey-syntax.yaml"></a>

```
  [EnforcementInRecord](#cfn-timestream-table-partitionkey-enforcementinrecord): String
  [Name](#cfn-timestream-table-partitionkey-name): String
  [Type](#cfn-timestream-table-partitionkey-type): String
```

## Properties<a name="aws-properties-timestream-table-partitionkey-properties"></a>

`EnforcementInRecord`  <a name="cfn-timestream-table-partitionkey-enforcementinrecord"></a>
 The level of enforcement for the specification of a dimension key in ingested records\. Options are REQUIRED \(dimension key must be specified\) and OPTIONAL \(dimension key does not have to be specified\)\.   
*Required*: No  
*Type*: String  
*Allowed values*: `OPTIONAL | REQUIRED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-timestream-table-partitionkey-name"></a>
 The name of the attribute used for a dimension key\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-timestream-table-partitionkey-type"></a>
 The type of the partition key\. Options are DIMENSION \(dimension key\) and MEASURE \(measure key\)\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `DIMENSION | MEASURE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)