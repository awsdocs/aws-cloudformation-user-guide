# AWS::QuickSight::Template PivotTableDataPathOption<a name="aws-properties-quicksight-template-pivottabledatapathoption"></a>

The data path options for the pivot table field options\.

## Syntax<a name="aws-properties-quicksight-template-pivottabledatapathoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-pivottabledatapathoption-syntax.json"></a>

```
{
  "[DataPathList](#cfn-quicksight-template-pivottabledatapathoption-datapathlist)" : [ DataPathValue, ... ],
  "[Width](#cfn-quicksight-template-pivottabledatapathoption-width)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-pivottabledatapathoption-syntax.yaml"></a>

```
  [DataPathList](#cfn-quicksight-template-pivottabledatapathoption-datapathlist): 
    - DataPathValue
  [Width](#cfn-quicksight-template-pivottabledatapathoption-width): String
```

## Properties<a name="aws-properties-quicksight-template-pivottabledatapathoption-properties"></a>

`DataPathList`  <a name="cfn-quicksight-template-pivottabledatapathoption-datapathlist"></a>
The list of data path values for the data path options\.  
*Required*: Yes  
*Type*: List of [DataPathValue](aws-properties-quicksight-template-datapathvalue.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Width`  <a name="cfn-quicksight-template-pivottabledatapathoption-width"></a>
The width of the data path option\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)