# AWS::QuickSight::DataSet LogicalTable<a name="aws-properties-quicksight-dataset-logicaltable"></a>

A *logical table* is a unit that joins and that data transformations operate on\. A logical table has a source, which can be either a physical table or result of a join\. When a logical table points to a physical table, the logical table acts as a mutable copy of that physical table through transform operations\.

## Syntax<a name="aws-properties-quicksight-dataset-logicaltable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-logicaltable-syntax.json"></a>

```
{
  "[Alias](#cfn-quicksight-dataset-logicaltable-alias)" : String,
  "[DataTransforms](#cfn-quicksight-dataset-logicaltable-datatransforms)" : [ TransformOperation, ... ],
  "[Source](#cfn-quicksight-dataset-logicaltable-source)" : LogicalTableSource
}
```

### YAML<a name="aws-properties-quicksight-dataset-logicaltable-syntax.yaml"></a>

```
  [Alias](#cfn-quicksight-dataset-logicaltable-alias): String
  [DataTransforms](#cfn-quicksight-dataset-logicaltable-datatransforms): 
    - TransformOperation
  [Source](#cfn-quicksight-dataset-logicaltable-source): 
    LogicalTableSource
```

## Properties<a name="aws-properties-quicksight-dataset-logicaltable-properties"></a>

`Alias`  <a name="cfn-quicksight-dataset-logicaltable-alias"></a>
A display name for the logical table\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataTransforms`  <a name="cfn-quicksight-dataset-logicaltable-datatransforms"></a>
Transform operations that act on this logical table\. For this structure to be valid, only one of the attributes can be non\-null\.   
*Required*: No  
*Type*: List of [TransformOperation](aws-properties-quicksight-dataset-transformoperation.md)  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source`  <a name="cfn-quicksight-dataset-logicaltable-source"></a>
Source of this logical table\.  
*Required*: Yes  
*Type*: [LogicalTableSource](aws-properties-quicksight-dataset-logicaltablesource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)