# AWS::QuickSight::Template DataSetSchema<a name="aws-properties-quicksight-template-datasetschema"></a>

Dataset schema\.

## Syntax<a name="aws-properties-quicksight-template-datasetschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-datasetschema-syntax.json"></a>

```
{
  "[ColumnSchemaList](#cfn-quicksight-template-datasetschema-columnschemalist)" : [ ColumnSchema, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-datasetschema-syntax.yaml"></a>

```
  [ColumnSchemaList](#cfn-quicksight-template-datasetschema-columnschemalist): 
    - ColumnSchema
```

## Properties<a name="aws-properties-quicksight-template-datasetschema-properties"></a>

`ColumnSchemaList`  <a name="cfn-quicksight-template-datasetschema-columnschemalist"></a>
A structure containing the list of column schemas\.  
*Required*: No  
*Type*: List of [ColumnSchema](aws-properties-quicksight-template-columnschema.md)  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)