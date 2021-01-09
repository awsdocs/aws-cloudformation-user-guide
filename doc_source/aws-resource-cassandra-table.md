# AWS::Cassandra::Table<a name="aws-resource-cassandra-table"></a>

The `AWS::Cassandra::Table` resource allows you to create a new table in Amazon Keyspaces \(for Apache Cassandra\)\. For more information, see [Create a Keyspace and a Table](https://docs.aws.amazon.com/keyspaces/latest/devguide/getting-started.ddl.html) in the *Amazon Keyspaces Developer Guide*\.

## Syntax<a name="aws-resource-cassandra-table-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cassandra-table-syntax.json"></a>

```
{
  "Type" : "AWS::Cassandra::Table",
  "Properties" : {
      "[BillingMode](#cfn-cassandra-table-billingmode)" : BillingMode,
      "[ClusteringKeyColumns](#cfn-cassandra-table-clusteringkeycolumns)" : [ ClusteringKeyColumn, ... ],
      "[KeyspaceName](#cfn-cassandra-table-keyspacename)" : String,
      "[PartitionKeyColumns](#cfn-cassandra-table-partitionkeycolumns)" : [ Column, ... ],
      "[RegularColumns](#cfn-cassandra-table-regularcolumns)" : [ Column, ... ],
      "[TableName](#cfn-cassandra-table-tablename)" : String
    }
}
```

### YAML<a name="aws-resource-cassandra-table-syntax.yaml"></a>

```
Type: AWS::Cassandra::Table
Properties: 
  [BillingMode](#cfn-cassandra-table-billingmode): 
    BillingMode
  [ClusteringKeyColumns](#cfn-cassandra-table-clusteringkeycolumns): 
    - ClusteringKeyColumn
  [KeyspaceName](#cfn-cassandra-table-keyspacename): String
  [PartitionKeyColumns](#cfn-cassandra-table-partitionkeycolumns): 
    - Column
  [RegularColumns](#cfn-cassandra-table-regularcolumns): 
    - Column
  [TableName](#cfn-cassandra-table-tablename): String
```

## Properties<a name="aws-resource-cassandra-table-properties"></a>

`BillingMode`  <a name="cfn-cassandra-table-billingmode"></a>
The billing mode for the table, which determines how you'll be charged for reads and writes:  
+ **On\-demand mode** \(default\) \- you pay based on the actual reads and writes your application performs\.
+ **Provisioned mode** \- lets you specify the number of reads and writes per second that you need for your application\.
If you don't specify a value for this property, then the table will use on\-demand mode\.  
*Required*: No  
*Type*: [BillingMode](aws-properties-cassandra-table-billingmode.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClusteringKeyColumns`  <a name="cfn-cassandra-table-clusteringkeycolumns"></a>
One or more columns that determine how the table data is sorted\.  
*Required*: No  
*Type*: List of [ClusteringKeyColumn](aws-properties-cassandra-table-clusteringkeycolumn.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KeyspaceName`  <a name="cfn-cassandra-table-keyspacename"></a>
The name of the keyspace in which to create the table\. The keyspace must already exist\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PartitionKeyColumns`  <a name="cfn-cassandra-table-partitionkeycolumns"></a>
One or more columns that uniquely identify every row in the table\. Every table must have a partition key\.  
*Required*: Yes  
*Type*: List of [Column](aws-properties-cassandra-table-column.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RegularColumns`  <a name="cfn-cassandra-table-regularcolumns"></a>
One or more columns that are not part of the primary key \- that is, columns that are *not* defined as partition key columns or clustering key columns\.  
*Required*: No  
*Type*: List of [Column](aws-properties-cassandra-table-column.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-cassandra-table-tablename"></a>
The name of the table to be created\. If you don't specify a name, AWS CloudFormation generates a unique ID and uses that ID for the table name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Length Constraints:* Minimum length of 3\. Maximum length of 255\.  
*Pattern:* `^[a-zA-Z0-9][a-zA-Z0-9_]{1,47}$`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cassandra-table-return-values"></a>

### Ref<a name="aws-resource-cassandra-table-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the table and the keyspace where the table exists \(delimited by '\|'\)\. For example:

 `{ "Ref": "myKeyspace|myTable" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-cassandra-table--examples"></a>



### Create a Table with Minimal Options<a name="aws-resource-cassandra-table--examples--Create_a_Table_with_Minimal_Options"></a>

The following example creates a new table\. The table will have a system\-generated name, and will use on\-demand billing\.

#### JSON<a name="aws-resource-cassandra-table--examples--Create_a_Table_with_Minimal_Options--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "MyNewTable": {
      "Type": "AWS::Cassandra::Table",
      "Properties": {
        "KeyspaceName": "MyNewKeyspace",
        "PartitionKeyColumns": [
          {
            "ColumnName": "Message",
            "ColumnType": "ASCII"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-cassandra-table--examples--Create_a_Table_with_Minimal_Options--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  MyNewTable:
    Type: 'AWS::Cassandra::Table'
    Properties:
      KeyspaceName: MyNewKeyspace
      PartitionKeyColumns:
        - ColumnName: Message
          ColumnType: ASCII
```

### Create a Table Using Provisioned Mode<a name="aws-resource-cassandra-table--examples--Create_a_Table_Using_Provisioned_Mode"></a>

The following example creates a table with specific read and write capacity\.

#### JSON<a name="aws-resource-cassandra-table--examples--Create_a_Table_Using_Provisioned_Mode--json"></a>

```
{
  "AWSTemplateFormatVersion":"2010-09-09",
  "Resources":{
    "mySecondTable":{
      "Type":"AWS::Cassandra::Table",
      "Properties":{
        "KeyspaceName":"MyNewKeyspace",
        "TableName":"Employees",
        "PartitionKeyColumns":[
          {
            "ColumnName":"id",
            "ColumnType":"ASCII"
          }
        ],
        "ClusteringKeyColumns":[
          {
            "Column":{
              "ColumnName":"division",
              "ColumnType":"ASCII"
            },
            "OrderBy":"ASC"
          }
        ],
        "RegularColumns":[
          {
            "ColumnName":"name",
            "ColumnType":"TEXT"
          },
          {
            "ColumnName":"region",
            "ColumnType":"TEXT"
          },
          {
            "ColumnName":"division",
            "ColumnType":"TEXT"
          },
          {
            "ColumnName":"project",
            "ColumnType":"TEXT"
          },
          {
            "ColumnName":"role",
            "ColumnType":"TEXT"
          },
          {
            "ColumnName":"pay_scale",
            "ColumnType":"TEXT"
          },
          {
            "ColumnName":"vacation_hrs",
            "ColumnType":"FLOAT"
          },
          {
            "ColumnName":"manager_id",
            "ColumnType":"TEXT"
          }
        ],
        "BillingMode":{
          "Mode":"PROVISIONED",
          "ProvisionedThroughput":{
            "ReadCapacityUnits":5,
            "WriteCapacityUnits":5
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-cassandra-table--examples--Create_a_Table_Using_Provisioned_Mode--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  mySecondTable:
    Type: AWS::Cassandra::Table
    Properties:
      KeyspaceName: MyNewKeyspace
      TableName: Employees
      PartitionKeyColumns:
      - ColumnName: id
        ColumnType: ASCII
      ClusteringKeyColumns:
      - Column:
          ColumnName: division
          ColumnType: ASCII
        OrderBy: ASC
      RegularColumns:
      - ColumnName: name
        ColumnType: TEXT
      - ColumnName: region
        ColumnType: TEXT
      - ColumnName: division
        ColumnType: TEXT
      - ColumnName: project
        ColumnType: TEXT
      - ColumnName: role
        ColumnType: TEXT
      - ColumnName: pay_scale
        ColumnType: TEXT
      - ColumnName: vacation_hrs
        ColumnType: FLOAT
      - ColumnName: manager_id
        ColumnType: TEXT
      BillingMode:
        Mode: PROVISIONED
        ProvisionedThroughput:
          ReadCapacityUnits: 5
          WriteCapacityUnits: 5
```