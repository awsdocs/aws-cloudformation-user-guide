# AWS::DMS::Endpoint KinesisSettings<a name="aws-properties-dms-endpoint-kinesissettings"></a>

Provides information that describes an Amazon Kinesis Data Stream endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\. For more information about other available settings, see [ Using object mapping to migrate data to a Kinesis data stream](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Kinesis.html#CHAP_Target.Kinesis.ObjectMapping) in the *AWS Database Migration Service User Guide*\.

## Syntax<a name="aws-properties-dms-endpoint-kinesissettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-kinesissettings-syntax.json"></a>

```
{
  "[IncludeControlDetails](#cfn-dms-endpoint-kinesissettings-includecontroldetails)" : Boolean,
  "[IncludeNullAndEmpty](#cfn-dms-endpoint-kinesissettings-includenullandempty)" : Boolean,
  "[IncludePartitionValue](#cfn-dms-endpoint-kinesissettings-includepartitionvalue)" : Boolean,
  "[IncludeTableAlterOperations](#cfn-dms-endpoint-kinesissettings-includetablealteroperations)" : Boolean,
  "[IncludeTransactionDetails](#cfn-dms-endpoint-kinesissettings-includetransactiondetails)" : Boolean,
  "[MessageFormat](#cfn-dms-endpoint-kinesissettings-messageformat)" : String,
  "[NoHexPrefix](#cfn-dms-endpoint-kinesissettings-nohexprefix)" : Boolean,
  "[PartitionIncludeSchemaTable](#cfn-dms-endpoint-kinesissettings-partitionincludeschematable)" : Boolean,
  "[ServiceAccessRoleArn](#cfn-dms-endpoint-kinesissettings-serviceaccessrolearn)" : String,
  "[StreamArn](#cfn-dms-endpoint-kinesissettings-streamarn)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-kinesissettings-syntax.yaml"></a>

```
  [IncludeControlDetails](#cfn-dms-endpoint-kinesissettings-includecontroldetails): Boolean
  [IncludeNullAndEmpty](#cfn-dms-endpoint-kinesissettings-includenullandempty): Boolean
  [IncludePartitionValue](#cfn-dms-endpoint-kinesissettings-includepartitionvalue): Boolean
  [IncludeTableAlterOperations](#cfn-dms-endpoint-kinesissettings-includetablealteroperations): Boolean
  [IncludeTransactionDetails](#cfn-dms-endpoint-kinesissettings-includetransactiondetails): Boolean
  [MessageFormat](#cfn-dms-endpoint-kinesissettings-messageformat): String
  [NoHexPrefix](#cfn-dms-endpoint-kinesissettings-nohexprefix): Boolean
  [PartitionIncludeSchemaTable](#cfn-dms-endpoint-kinesissettings-partitionincludeschematable): Boolean
  [ServiceAccessRoleArn](#cfn-dms-endpoint-kinesissettings-serviceaccessrolearn): String
  [StreamArn](#cfn-dms-endpoint-kinesissettings-streamarn): String
```

## Properties<a name="aws-properties-dms-endpoint-kinesissettings-properties"></a>

`IncludeControlDetails`  <a name="cfn-dms-endpoint-kinesissettings-includecontroldetails"></a>
Shows detailed control information for table definition, column definition, and table and column changes in the Kinesis message output\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeNullAndEmpty`  <a name="cfn-dms-endpoint-kinesissettings-includenullandempty"></a>
Include NULL and empty columns for records migrated to the endpoint\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludePartitionValue`  <a name="cfn-dms-endpoint-kinesissettings-includepartitionvalue"></a>
Shows the partition value within the Kinesis message output, unless the partition type is `schema-table-type`\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeTableAlterOperations`  <a name="cfn-dms-endpoint-kinesissettings-includetablealteroperations"></a>
Includes any data definition language \(DDL\) operations that change the table in the control data, such as `rename-table`, `drop-table`, `add-column`, `drop-column`, and `rename-column`\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeTransactionDetails`  <a name="cfn-dms-endpoint-kinesissettings-includetransactiondetails"></a>
Provides detailed transaction information from the source database\. This information includes a commit timestamp, a log position, and values for `transaction_id`, previous `transaction_id`, and `transaction_record_id` \(the record offset within a transaction\)\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageFormat`  <a name="cfn-dms-endpoint-kinesissettings-messageformat"></a>
The output format for the records created on the endpoint\. The message format is `JSON` \(default\) or `JSON_UNFORMATTED` \(a single line with no tab\)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `json | json-unformatted`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoHexPrefix`  <a name="cfn-dms-endpoint-kinesissettings-nohexprefix"></a>
Set this optional parameter to `true` to avoid adding a '0x' prefix to raw data in hexadecimal format\. For example, by default, AWS DMS adds a '0x' prefix to the LOB column type in hexadecimal format moving from an Oracle source to an Amazon Kinesis target\. Use the `NoHexPrefix` endpoint setting to enable migration of RAW data type columns without adding the '0x' prefix\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PartitionIncludeSchemaTable`  <a name="cfn-dms-endpoint-kinesissettings-partitionincludeschematable"></a>
Prefixes schema and table names to partition values, when the partition type is `primary-key-type`\. Doing this increases data distribution among Kinesis shards\. For example, suppose that a SysBench schema has thousands of tables and each table has only limited range for a primary key\. In this case, the same primary key is sent from thousands of tables to the same shard, which causes throttling\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceAccessRoleArn`  <a name="cfn-dms-endpoint-kinesissettings-serviceaccessrolearn"></a>
The Amazon Resource Name \(ARN\) for the IAM role that AWS DMS uses to write to the Kinesis data stream\. The role must allow the `iam:PassRole` action\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamArn`  <a name="cfn-dms-endpoint-kinesissettings-streamarn"></a>
The Amazon Resource Name \(ARN\) for the Amazon Kinesis Data Streams endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)