# AWS::QuickSight::Analysis AxisLabelReferenceOptions<a name="aws-properties-quicksight-analysis-axislabelreferenceoptions"></a>

The reference that specifies where the axis label is applied to\.

## Syntax<a name="aws-properties-quicksight-analysis-axislabelreferenceoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-axislabelreferenceoptions-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-analysis-axislabelreferenceoptions-column)" : ColumnIdentifier,
  "[FieldId](#cfn-quicksight-analysis-axislabelreferenceoptions-fieldid)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-axislabelreferenceoptions-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-analysis-axislabelreferenceoptions-column): 
    ColumnIdentifier
  [FieldId](#cfn-quicksight-analysis-axislabelreferenceoptions-fieldid): String
```

## Properties<a name="aws-properties-quicksight-analysis-axislabelreferenceoptions-properties"></a>

`Column`  <a name="cfn-quicksight-analysis-axislabelreferenceoptions-column"></a>
The column that the axis label is targeted to\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-analysis-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-analysis-axislabelreferenceoptions-fieldid"></a>
The field that the axis label is targeted to\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)