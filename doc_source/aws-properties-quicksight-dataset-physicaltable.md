# AWS::QuickSight::DataSet PhysicalTable<a name="aws-properties-quicksight-dataset-physicaltable"></a>

A view of a data source that contains information about the shape of the data in the underlying source\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.

## Syntax<a name="aws-properties-quicksight-dataset-physicaltable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-physicaltable-syntax.json"></a>

```
{
  "[CustomSql](#cfn-quicksight-dataset-physicaltable-customsql)" : CustomSql,
  "[RelationalTable](#cfn-quicksight-dataset-physicaltable-relationaltable)" : RelationalTable,
  "[S3Source](#cfn-quicksight-dataset-physicaltable-s3source)" : S3Source
}
```

### YAML<a name="aws-properties-quicksight-dataset-physicaltable-syntax.yaml"></a>

```
  [CustomSql](#cfn-quicksight-dataset-physicaltable-customsql): 
    CustomSql
  [RelationalTable](#cfn-quicksight-dataset-physicaltable-relationaltable): 
    RelationalTable
  [S3Source](#cfn-quicksight-dataset-physicaltable-s3source): 
    S3Source
```

## Properties<a name="aws-properties-quicksight-dataset-physicaltable-properties"></a>

`CustomSql`  <a name="cfn-quicksight-dataset-physicaltable-customsql"></a>
A physical table type built from the results of the custom SQL query\.  
*Required*: No  
*Type*: [CustomSql](aws-properties-quicksight-dataset-customsql.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelationalTable`  <a name="cfn-quicksight-dataset-physicaltable-relationaltable"></a>
A physical table type for relational data sources\.  
*Required*: No  
*Type*: [RelationalTable](aws-properties-quicksight-dataset-relationaltable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Source`  <a name="cfn-quicksight-dataset-physicaltable-s3source"></a>
A physical table type for as S3 data source\.  
*Required*: No  
*Type*: [S3Source](aws-properties-quicksight-dataset-s3source.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)