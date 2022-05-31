# AWS::Cassandra::Table<a name="aws-resource-cassandra-table"></a>

The `AWS::Cassandra::Table` resource allows you to create a new table in Amazon Keyspaces \(for Apache Cassandra\)\. For more information, see [Create a keyspace and a table](https://docs.aws.amazon.com/keyspaces/latest/devguide/getting-started.ddl.html) in the *Amazon Keyspaces Developer Guide*\.

## Syntax<a name="aws-resource-cassandra-table-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cassandra-table-syntax.json"></a>

```
{
  "Type" : "AWS::Cassandra::Table",
  "Properties" : {
      "[BillingMode](#cfn-cassandra-table-billingmode)" : BillingMode,
      "[ClusteringKeyColumns](#cfn-cassandra-table-clusteringkeycolumns)" : [ ClusteringKeyColumn, ... ],
      "[DefaultTimeToLive](#cfn-cassandra-table-defaulttimetolive)" : Integer,
      "[EncryptionSpecification](#cfn-cassandra-table-encryptionspecification)" : EncryptionSpecification,
      "[KeyspaceName](#cfn-cassandra-table-keyspacename)" : String,
      "[PartitionKeyColumns](#cfn-cassandra-table-partitionkeycolumns)" : [ Column, ... ],
      "[PointInTimeRecoveryEnabled](#cfn-cassandra-table-pointintimerecoveryenabled)" : Boolean,
      "[RegularColumns](#cfn-cassandra-table-regularcolumns)" : [ Column, ... ],
      "[TableName](#cfn-cassandra-table-tablename)" : String,
      "[Tags](#cfn-cassandra-table-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
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
  [DefaultTimeToLive](#cfn-cassandra-table-defaulttimetolive): Integer
  [EncryptionSpecification](#cfn-cassandra-table-encryptionspecification): 
    EncryptionSpecification
  [KeyspaceName](#cfn-cassandra-table-keyspacename): String
  [PartitionKeyColumns](#cfn-cassandra-table-partitionkeycolumns): 
    - Column
  [PointInTimeRecoveryEnabled](#cfn-cassandra-table-pointintimerecoveryenabled): Boolean
  [RegularColumns](#cfn-cassandra-table-regularcolumns): 
    - Column
  [TableName](#cfn-cassandra-table-tablename): String
  [Tags](#cfn-cassandra-table-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-cassandra-table-properties"></a>

`BillingMode`  <a name="cfn-cassandra-table-billingmode"></a>
The billing mode for the table, which determines how you'll be charged for reads and writes:  
+ **On\-demand mode** \(default\) \- You pay based on the actual reads and writes your application performs\.
+ **Provisioned mode** \- Lets you specify the number of reads and writes per second that you need for your application\.
If you don't specify a value for this property, then the table will use on\-demand mode\.  
*Required*: No  
*Type*: [BillingMode](aws-properties-cassandra-table-billingmode.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClusteringKeyColumns`  <a name="cfn-cassandra-table-clusteringkeycolumns"></a>
One or more columns that determine how the table data is sorted\.  
*Required*: No  
*Type*: List of [ClusteringKeyColumn](aws-properties-cassandra-table-clusteringkeycolumn.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DefaultTimeToLive`  <a name="cfn-cassandra-table-defaulttimetolive"></a>
The default Time To Live \(TTL\) value for all rows in a table in seconds\. The maximum configurable value is 630,720,000 seconds, which is the equivalent of 20 years\. By default, the TTL value for a table is 0, which means data does not expire\.   
For more information, see [Setting the default TTL value for a table](https://docs.aws.amazon.com/keyspaces/latest/devguide/TTL-how-it-works.html#ttl-howitworks_default_ttl) in the *Amazon Keyspaces Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionSpecification`  <a name="cfn-cassandra-table-encryptionspecification"></a>
The encryption at rest options for the table\.  
+ **AWS owned key** \(default\) \- The key is owned by Amazon Keyspaces\.
+ **Customer managed key** \- The key is stored in your account and is created, owned, and managed by you\.
**Note**  
If you choose encryption with a customer managed key, you must specify a valid customer managed KMS key with permissions granted to Amazon Keyspaces\.
For more information, see [Encryption at rest in Amazon Keyspaces](https://docs.aws.amazon.com/keyspaces/latest/devguide/EncryptionAtRest.html) in the *Amazon Keyspaces Developer Guide*\.  
*Required*: No  
*Type*: [EncryptionSpecification](aws-properties-cassandra-table-encryptionspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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

`PointInTimeRecoveryEnabled`  <a name="cfn-cassandra-table-pointintimerecoveryenabled"></a>
Specifies if point\-in\-time recovery is enabled or disabled for the table\. The options are `PointInTimeRecoveryEnabled=true` and `PointInTimeRecoveryEnabled=false`\. If not specified, the default is `PointInTimeRecoveryEnabled=false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegularColumns`  <a name="cfn-cassandra-table-regularcolumns"></a>
One or more columns that are not part of the primary key \- that is, columns that are *not* defined as partition key columns or clustering key columns\.  
You can add regular columns to existing tables by adding them to the template\.  
*Required*: No  
*Type*: List of [Column](aws-properties-cassandra-table-column.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-cassandra-table-tablename"></a>
The name of the table to be created\. The table name is case sensitive\. If you don't specify a name, AWS CloudFormation generates a unique ID and uses that ID for the table name\. For more information, see [Name type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Length constraints:* Minimum length of 3\. Maximum length of 255\.  
*Pattern:* `^[a-zA-Z0-9][a-zA-Z0-9_]{1,47}$`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-cassandra-table-tags"></a>
A list of key\-value pair tags to be attached to the resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cassandra-table-return-values"></a>

### Ref<a name="aws-resource-cassandra-table-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the table and the keyspace where the table exists \(delimited by '\|'\)\. For example:

 `{ "Ref": "myKeyspace|myTable" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-cassandra-table--examples"></a>



### Create a table with minimal options<a name="aws-resource-cassandra-table--examples--Create_a_table_with_minimal_options"></a>

The following example creates a new table\. The table will have a system\-generated name, and will use on\-demand billing\.

#### JSON<a name="aws-resource-cassandra-table--examples--Create_a_table_with_minimal_options--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "myNewTable": {
      "Type": "AWS::Cassandra::Table",
      "Properties": {
        "KeyspaceName": "my_keyspace",
        "TableName":"my_table",
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

#### YAML<a name="aws-resource-cassandra-table--examples--Create_a_table_with_minimal_options--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myNewTable:
    Type: 'AWS::Cassandra::Table'
    Properties:
      KeyspaceName: my_keyspace
      TableName: my_table
      PartitionKeyColumns:
        - ColumnName: Message
          ColumnType: ASCII
```

### Create a table using all options<a name="aws-resource-cassandra-table--examples--Create_a_table_using_all_options"></a>

The following example creates a table `my_table` with all available properties\. For example, provisioned read and write capacity, default TTL, encryption settings, PITR, and tags\. To use this sample, you must replace the key ARN in the example with your own\.

#### JSON<a name="aws-resource-cassandra-table--examples--Create_a_table_using_all_options--json"></a>

```
{
   "AWSTemplateFormatVersion":"2010-09-09",
   "Resources":{
      "myNewTable":{
         "Type":"AWS::Cassandra::Table",
         "Properties":{
            "KeyspaceName":"my_keyspace",
            "TableName":"my_table",
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
            },
            "DefaultTimeToLive":63072000,
            "EncryptionSpecification":{
               "EncryptionType":"CUSTOMER_MANAGED_KMS_KEY",
               "KmsKeyIdentifier":"<emphasis>arn:aws:kms:eu-west-1:5555555555555:key/11111111-1111-111-1111-111111111111</emphasis>"
              }
            },
            "PointInTimeRecoveryEnabled":true,
            "Tags":[
            {
               "Key":"tag1",
               "Value":"val1"
            },
            {
               "Key":"tag2",
               "Value":"val2"
            }
         ]
      }
   }
}
```

#### YAML<a name="aws-resource-cassandra-table--examples--Create_a_table_using_all_options--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myNewTable:
    Type: AWS::Cassandra::Table
    Properties:
      KeyspaceName: my_keyspace
      TableName: my_table
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
      DefaultTimeToLive: 63072000
      EncryptionSpecification:
        EncryptionType: CUSTOMER_MANAGED_KMS_KEY
        KmsKeyIdentifier: arn:aws:kms:eu-west-1:5555555555555:key/11111111-1111-111-1111-111111111111
      PointInTimeRecoveryEnabled: true
      Tags:
        - Key: tag1
          Value: val1
        - Key: tag2
          Value: val2
```

### Add new columns to an existing table<a name="aws-resource-cassandra-table--examples--Add_new_columns_to_an_existing_table"></a>

The following example shows how to add five new columns to the existing table `my_table`\. Only regular columns can be added to a table\.

#### JSON<a name="aws-resource-cassandra-table--examples--Add_new_columns_to_an_existing_table--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "myTable": {
      "Type": "AWS::Cassandra::Table",
      "Properties": {
        "KeyspaceName": "my_keyspace",
        "TableName":"my_table",
        "PartitionKeyColumns": [
          {
            "ColumnName": "Message",
            "ColumnType": "ASCII"
          }
        ],
        "RegularColumns": [
          {
            "ColumnName": "name",
            "ColumnType": "TEXT"
          },
          {
            "ColumnName": "region",
            "ColumnType": "TEXT"
          }
        ]
      }
    }
  }
}
```

#### JSON<a name="aws-resource-cassandra-table--examples--Add_new_columns_to_an_existing_table--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "myTable": {
      "Type": "AWS::Cassandra::Table",
      "Properties": {
        "KeyspaceName": "my_keyspace",
        "TableName":"my_table",
        "PartitionKeyColumns": [
          {
            "ColumnName": "Message",
            "ColumnType": "ASCII"
          }
        ],
        "RegularColumns": [
          {
            "ColumnName": "name",
            "ColumnType": "TEXT"
          },
          {
            "ColumnName": "region",
            "ColumnType": "TEXT"
          },
          {
            "ColumnName": "project",
            "ColumnType": "TEXT"
          },
          {
            "ColumnName": "role",
            "ColumnType": "TEXT"
          },
          {
            "ColumnName": "pay_scale",
            "ColumnType": "TEXT"
          },
          {
            "ColumnName": "vacation_hrs",
            "ColumnType": "FLOAT"
          },
          {
            "ColumnName": "manager_id",
            "ColumnType": "TEXT"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-cassandra-table--examples--Add_new_columns_to_an_existing_table--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myTable:
    Type: 'AWS::Cassandra::Table'
    Properties:
      KeyspaceName: my_keyspace
      TableName: my_table
      PartitionKeyColumns:
        - ColumnName: Message
          ColumnType: ASCII
      RegularColumns:
        - ColumnName: name
          ColumnType: TEXT
        - ColumnName: region
          ColumnType: TEXT
```

#### YAML<a name="aws-resource-cassandra-table--examples--Add_new_columns_to_an_existing_table--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myTable:
    Type: 'AWS::Cassandra::Table'
    Properties:
      KeyspaceName: my_keyspace
      TableName: my_table
      PartitionKeyColumns:
        - ColumnName: Message
          ColumnType: ASCII
      RegularColumns:
        - ColumnName: name
          ColumnType: TEXT
        - ColumnName: region
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
```