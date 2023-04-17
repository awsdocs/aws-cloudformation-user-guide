# AWS::QuickSight::Template CategoricalDimensionField<a name="aws-properties-quicksight-template-categoricaldimensionfield"></a>

The dimension type field with categorical type columns\.\.

## Syntax<a name="aws-properties-quicksight-template-categoricaldimensionfield-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-categoricaldimensionfield-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-template-categoricaldimensionfield-column)" : ColumnIdentifier,
  "[FieldId](#cfn-quicksight-template-categoricaldimensionfield-fieldid)" : String,
  "[FormatConfiguration](#cfn-quicksight-template-categoricaldimensionfield-formatconfiguration)" : StringFormatConfiguration,
  "[HierarchyId](#cfn-quicksight-template-categoricaldimensionfield-hierarchyid)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-categoricaldimensionfield-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-template-categoricaldimensionfield-column): 
    ColumnIdentifier
  [FieldId](#cfn-quicksight-template-categoricaldimensionfield-fieldid): String
  [FormatConfiguration](#cfn-quicksight-template-categoricaldimensionfield-formatconfiguration): 
    StringFormatConfiguration
  [HierarchyId](#cfn-quicksight-template-categoricaldimensionfield-hierarchyid): String
```

## Properties<a name="aws-properties-quicksight-template-categoricaldimensionfield-properties"></a>

`Column`  <a name="cfn-quicksight-template-categoricaldimensionfield-column"></a>
The column that is used in the `CategoricalDimensionField`\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-template-categoricaldimensionfield-fieldid"></a>
The custom field ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FormatConfiguration`  <a name="cfn-quicksight-template-categoricaldimensionfield-formatconfiguration"></a>
The format configuration of the field\.  
*Required*: No  
*Type*: [StringFormatConfiguration](aws-properties-quicksight-template-stringformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HierarchyId`  <a name="cfn-quicksight-template-categoricaldimensionfield-hierarchyid"></a>
The custom hierarchy ID\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)