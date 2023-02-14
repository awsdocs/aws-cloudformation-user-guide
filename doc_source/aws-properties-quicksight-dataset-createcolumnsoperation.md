# AWS::QuickSight::DataSet CreateColumnsOperation<a name="aws-properties-quicksight-dataset-createcolumnsoperation"></a>

A transform operation that creates calculated columns\. Columns created in one such operation form a lexical closure\.

## Syntax<a name="aws-properties-quicksight-dataset-createcolumnsoperation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-createcolumnsoperation-syntax.json"></a>

```
{
  "[Columns](#cfn-quicksight-dataset-createcolumnsoperation-columns)" : [ CalculatedColumn, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dataset-createcolumnsoperation-syntax.yaml"></a>

```
  [Columns](#cfn-quicksight-dataset-createcolumnsoperation-columns): 
    - CalculatedColumn
```

## Properties<a name="aws-properties-quicksight-dataset-createcolumnsoperation-properties"></a>

`Columns`  <a name="cfn-quicksight-dataset-createcolumnsoperation-columns"></a>
Calculated columns to create\.  
*Required*: Yes  
*Type*: List of [CalculatedColumn](aws-properties-quicksight-dataset-calculatedcolumn.md)  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)