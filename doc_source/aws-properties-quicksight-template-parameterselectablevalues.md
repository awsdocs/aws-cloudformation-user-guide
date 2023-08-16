# AWS::QuickSight::Template ParameterSelectableValues<a name="aws-properties-quicksight-template-parameterselectablevalues"></a>

A list of selectable values that are used in a control\.

## Syntax<a name="aws-properties-quicksight-template-parameterselectablevalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-parameterselectablevalues-syntax.json"></a>

```
{
  "[LinkToDataSetColumn](#cfn-quicksight-template-parameterselectablevalues-linktodatasetcolumn)" : ColumnIdentifier,
  "[Values](#cfn-quicksight-template-parameterselectablevalues-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-parameterselectablevalues-syntax.yaml"></a>

```
  [LinkToDataSetColumn](#cfn-quicksight-template-parameterselectablevalues-linktodatasetcolumn): 
    ColumnIdentifier
  [Values](#cfn-quicksight-template-parameterselectablevalues-values): 
    - String
```

## Properties<a name="aws-properties-quicksight-template-parameterselectablevalues-properties"></a>

`LinkToDataSetColumn`  <a name="cfn-quicksight-template-parameterselectablevalues-linktodatasetcolumn"></a>
The column identifier that fetches values from the data set\.  
*Required*: No  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-template-parameterselectablevalues-values"></a>
The values that are used in `ParameterSelectableValues`\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)