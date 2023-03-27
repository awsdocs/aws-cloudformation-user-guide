# AWS::QuickSight::Template ColumnGroupSchema<a name="aws-properties-quicksight-template-columngroupschema"></a>

The column group schema\.

## Syntax<a name="aws-properties-quicksight-template-columngroupschema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-columngroupschema-syntax.json"></a>

```
{
  "[ColumnGroupColumnSchemaList](#cfn-quicksight-template-columngroupschema-columngroupcolumnschemalist)" : [ ColumnGroupColumnSchema, ... ],
  "[Name](#cfn-quicksight-template-columngroupschema-name)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-columngroupschema-syntax.yaml"></a>

```
  [ColumnGroupColumnSchemaList](#cfn-quicksight-template-columngroupschema-columngroupcolumnschemalist): 
    - ColumnGroupColumnSchema
  [Name](#cfn-quicksight-template-columngroupschema-name): String
```

## Properties<a name="aws-properties-quicksight-template-columngroupschema-properties"></a>

`ColumnGroupColumnSchemaList`  <a name="cfn-quicksight-template-columngroupschema-columngroupcolumnschemalist"></a>
A structure containing the list of schemas for column group columns\.  
*Required*: No  
*Type*: List of [ColumnGroupColumnSchema](aws-properties-quicksight-template-columngroupcolumnschema.md)  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-template-columngroupschema-name"></a>
The name of the column group schema\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)