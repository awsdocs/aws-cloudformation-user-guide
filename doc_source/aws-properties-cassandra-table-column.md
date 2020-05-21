# AWS::Cassandra::Table Column<a name="aws-properties-cassandra-table-column"></a>

The name and data type of an individual column in a table\.

## Syntax<a name="aws-properties-cassandra-table-column-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cassandra-table-column-syntax.json"></a>

```
{
  "[ColumnName](#cfn-cassandra-table-column-columnname)" : String,
  "[ColumnType](#cfn-cassandra-table-column-columntype)" : String
}
```

### YAML<a name="aws-properties-cassandra-table-column-syntax.yaml"></a>

```
  [ColumnName](#cfn-cassandra-table-column-columnname): String
  [ColumnType](#cfn-cassandra-table-column-columntype): String
```

## Properties<a name="aws-properties-cassandra-table-column-properties"></a>

`ColumnName`  <a name="cfn-cassandra-table-column-columnname"></a>
The name of the column\. For more information, see [Identifiers](https://docs.aws.amazon.com/keyspaces/latest/devguide/cql.elements.html#cql.elements.identifier) in the *Amazon Keyspaces Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnType`  <a name="cfn-cassandra-table-column-columntype"></a>
The data type of the column\. For more information, see [Data Types](https://docs.aws.amazon.com/keyspaces/latest/devguide/cql.elements.html#cql.data-types) in the the *Amazon Keyspaces Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)