# AWS::QuickSight::DataSet CustomSql<a name="aws-properties-quicksight-dataset-customsql"></a>

A physical table type built from the results of the custom SQL query\.

## Syntax<a name="aws-properties-quicksight-dataset-customsql-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-customsql-syntax.json"></a>

```
{
  "[Columns](#cfn-quicksight-dataset-customsql-columns)" : [ InputColumn, ... ],
  "[DataSourceArn](#cfn-quicksight-dataset-customsql-datasourcearn)" : String,
  "[Name](#cfn-quicksight-dataset-customsql-name)" : String,
  "[SqlQuery](#cfn-quicksight-dataset-customsql-sqlquery)" : String
}
```

### YAML<a name="aws-properties-quicksight-dataset-customsql-syntax.yaml"></a>

```
  [Columns](#cfn-quicksight-dataset-customsql-columns): 
    - InputColumn
  [DataSourceArn](#cfn-quicksight-dataset-customsql-datasourcearn): String
  [Name](#cfn-quicksight-dataset-customsql-name): String
  [SqlQuery](#cfn-quicksight-dataset-customsql-sqlquery): String
```

## Properties<a name="aws-properties-quicksight-dataset-customsql-properties"></a>

`Columns`  <a name="cfn-quicksight-dataset-customsql-columns"></a>
The column schema from the SQL query result set\.  
*Required*: Yes  
*Type*: List of [InputColumn](aws-properties-quicksight-dataset-inputcolumn.md)  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSourceArn`  <a name="cfn-quicksight-dataset-customsql-datasourcearn"></a>
The Amazon Resource Name \(ARN\) of the data source\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-dataset-customsql-name"></a>
A display name for the SQL query result\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqlQuery`  <a name="cfn-quicksight-dataset-customsql-sqlquery"></a>
The SQL query\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `65536`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)