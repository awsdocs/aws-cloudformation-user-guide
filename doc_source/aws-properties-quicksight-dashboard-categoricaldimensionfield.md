# AWS::QuickSight::Dashboard CategoricalDimensionField<a name="aws-properties-quicksight-dashboard-categoricaldimensionfield"></a>

The dimension type field with categorical type columns\.\.

## Syntax<a name="aws-properties-quicksight-dashboard-categoricaldimensionfield-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-categoricaldimensionfield-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-dashboard-categoricaldimensionfield-column)" : ColumnIdentifier,
  "[FieldId](#cfn-quicksight-dashboard-categoricaldimensionfield-fieldid)" : String,
  "[FormatConfiguration](#cfn-quicksight-dashboard-categoricaldimensionfield-formatconfiguration)" : StringFormatConfiguration,
  "[HierarchyId](#cfn-quicksight-dashboard-categoricaldimensionfield-hierarchyid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-categoricaldimensionfield-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-dashboard-categoricaldimensionfield-column): 
    ColumnIdentifier
  [FieldId](#cfn-quicksight-dashboard-categoricaldimensionfield-fieldid): String
  [FormatConfiguration](#cfn-quicksight-dashboard-categoricaldimensionfield-formatconfiguration): 
    StringFormatConfiguration
  [HierarchyId](#cfn-quicksight-dashboard-categoricaldimensionfield-hierarchyid): String
```

## Properties<a name="aws-properties-quicksight-dashboard-categoricaldimensionfield-properties"></a>

`Column`  <a name="cfn-quicksight-dashboard-categoricaldimensionfield-column"></a>
The column that is used in the `CategoricalDimensionField`\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-dashboard-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-dashboard-categoricaldimensionfield-fieldid"></a>
The custom field ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FormatConfiguration`  <a name="cfn-quicksight-dashboard-categoricaldimensionfield-formatconfiguration"></a>
The format configuration of the field\.  
*Required*: No  
*Type*: [StringFormatConfiguration](aws-properties-quicksight-dashboard-stringformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HierarchyId`  <a name="cfn-quicksight-dashboard-categoricaldimensionfield-hierarchyid"></a>
The custom hierarchy ID\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)