# AWS::QuickSight::Analysis DateDimensionField<a name="aws-properties-quicksight-analysis-datedimensionfield"></a>

The dimension type field with date type columns\.

## Syntax<a name="aws-properties-quicksight-analysis-datedimensionfield-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-datedimensionfield-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-analysis-datedimensionfield-column)" : ColumnIdentifier,
  "[DateGranularity](#cfn-quicksight-analysis-datedimensionfield-dategranularity)" : String,
  "[FieldId](#cfn-quicksight-analysis-datedimensionfield-fieldid)" : String,
  "[FormatConfiguration](#cfn-quicksight-analysis-datedimensionfield-formatconfiguration)" : DateTimeFormatConfiguration,
  "[HierarchyId](#cfn-quicksight-analysis-datedimensionfield-hierarchyid)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-datedimensionfield-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-analysis-datedimensionfield-column): 
    ColumnIdentifier
  [DateGranularity](#cfn-quicksight-analysis-datedimensionfield-dategranularity): String
  [FieldId](#cfn-quicksight-analysis-datedimensionfield-fieldid): String
  [FormatConfiguration](#cfn-quicksight-analysis-datedimensionfield-formatconfiguration): 
    DateTimeFormatConfiguration
  [HierarchyId](#cfn-quicksight-analysis-datedimensionfield-hierarchyid): String
```

## Properties<a name="aws-properties-quicksight-analysis-datedimensionfield-properties"></a>

`Column`  <a name="cfn-quicksight-analysis-datedimensionfield-column"></a>
The column that is used in the `DateDimensionField`\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-analysis-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DateGranularity`  <a name="cfn-quicksight-analysis-datedimensionfield-dategranularity"></a>
The date granularity of the `DateDimensionField`\. Choose one of the following options:  
+  `YEAR` 
+  `QUARTER` 
+  `MONTH` 
+  `WEEK` 
+  `DAY` 
+  `HOUR` 
+  `MINUTE` 
+  `SECOND` 
+  `MILLISECOND` 
*Required*: No  
*Type*: String  
*Allowed values*: `DAY | HOUR | MILLISECOND | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-analysis-datedimensionfield-fieldid"></a>
The custom field ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FormatConfiguration`  <a name="cfn-quicksight-analysis-datedimensionfield-formatconfiguration"></a>
The format configuration of the field\.  
*Required*: No  
*Type*: [DateTimeFormatConfiguration](aws-properties-quicksight-analysis-datetimeformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HierarchyId`  <a name="cfn-quicksight-analysis-datedimensionfield-hierarchyid"></a>
The custom hierarchy ID\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)