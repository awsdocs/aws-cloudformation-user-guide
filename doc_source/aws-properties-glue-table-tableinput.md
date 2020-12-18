# AWS::Glue::Table TableInput<a name="aws-properties-glue-table-tableinput"></a>

A structure used to define a table\.

## Syntax<a name="aws-properties-glue-table-tableinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-tableinput-syntax.json"></a>

```
{
  "[Description](#cfn-glue-table-tableinput-description)" : String,
  "[Name](#cfn-glue-table-tableinput-name)" : String,
  "[Owner](#cfn-glue-table-tableinput-owner)" : String,
  "[Parameters](#cfn-glue-table-tableinput-parameters)" : Json,
  "[PartitionKeys](#cfn-glue-table-tableinput-partitionkeys)" : [ Column, ... ],
  "[Retention](#cfn-glue-table-tableinput-retention)" : Integer,
  "[StorageDescriptor](#cfn-glue-table-tableinput-storagedescriptor)" : StorageDescriptor,
  "[TableType](#cfn-glue-table-tableinput-tabletype)" : String,
  "[TargetTable](#cfn-glue-table-tableinput-targettable)" : TableIdentifier,
  "[ViewExpandedText](#cfn-glue-table-tableinput-viewexpandedtext)" : String,
  "[ViewOriginalText](#cfn-glue-table-tableinput-vieworiginaltext)" : String
}
```

### YAML<a name="aws-properties-glue-table-tableinput-syntax.yaml"></a>

```
  [Description](#cfn-glue-table-tableinput-description): String
  [Name](#cfn-glue-table-tableinput-name): String
  [Owner](#cfn-glue-table-tableinput-owner): String
  [Parameters](#cfn-glue-table-tableinput-parameters): Json
  [PartitionKeys](#cfn-glue-table-tableinput-partitionkeys): 
    - Column
  [Retention](#cfn-glue-table-tableinput-retention): Integer
  [StorageDescriptor](#cfn-glue-table-tableinput-storagedescriptor): 
    StorageDescriptor
  [TableType](#cfn-glue-table-tableinput-tabletype): String
  [TargetTable](#cfn-glue-table-tableinput-targettable): 
    TableIdentifier
  [ViewExpandedText](#cfn-glue-table-tableinput-viewexpandedtext): String
  [ViewOriginalText](#cfn-glue-table-tableinput-vieworiginaltext): String
```

## Properties<a name="aws-properties-glue-table-tableinput-properties"></a>

`Description`  <a name="cfn-glue-table-tableinput-description"></a>
A description of the table\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-table-tableinput-name"></a>
The table name\. For Hive compatibility, this is folded to lowercase when it is stored\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Owner`  <a name="cfn-glue-table-tableinput-owner"></a>
The table owner\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-glue-table-tableinput-parameters"></a>
These key\-value pairs define properties associated with the table\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PartitionKeys`  <a name="cfn-glue-table-tableinput-partitionkeys"></a>
A list of columns by which the table is partitioned\. Only primitive types are supported as partition keys\.  
When you create a table used by Amazon Athena, and you do not specify any `partitionKeys`, you must at least set the value of `partitionKeys` to an empty list\. For example:  
 `"PartitionKeys": []`   
*Required*: No  
*Type*: List of [Column](aws-properties-glue-table-column.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Retention`  <a name="cfn-glue-table-tableinput-retention"></a>
The retention time for this table\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageDescriptor`  <a name="cfn-glue-table-tableinput-storagedescriptor"></a>
A storage descriptor containing information about the physical storage of this table\.  
*Required*: No  
*Type*: [StorageDescriptor](aws-properties-glue-table-storagedescriptor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableType`  <a name="cfn-glue-table-tableinput-tabletype"></a>
The type of this table \(`EXTERNAL_TABLE`, `VIRTUAL_VIEW`, etc\.\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetTable`  <a name="cfn-glue-table-tableinput-targettable"></a>
A `TableIdentifier` structure that describes a target table for resource linking\.  
*Required*: No  
*Type*: [TableIdentifier](aws-properties-glue-table-tableidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ViewExpandedText`  <a name="cfn-glue-table-tableinput-viewexpandedtext"></a>
If the table is a view, the expanded text of the view; otherwise `null`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ViewOriginalText`  <a name="cfn-glue-table-tableinput-vieworiginaltext"></a>
If the table is a view, the original text of the view; otherwise `null`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)