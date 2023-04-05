# AWS::QuickSight::Analysis CascadingControlSource<a name="aws-properties-quicksight-analysis-cascadingcontrolsource"></a>

The source controls that are used in a `CascadingControlConfiguration`\.

## Syntax<a name="aws-properties-quicksight-analysis-cascadingcontrolsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-cascadingcontrolsource-syntax.json"></a>

```
{
  "[ColumnToMatch](#cfn-quicksight-analysis-cascadingcontrolsource-columntomatch)" : ColumnIdentifier,
  "[SourceSheetControlId](#cfn-quicksight-analysis-cascadingcontrolsource-sourcesheetcontrolid)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-cascadingcontrolsource-syntax.yaml"></a>

```
  [ColumnToMatch](#cfn-quicksight-analysis-cascadingcontrolsource-columntomatch): 
    ColumnIdentifier
  [SourceSheetControlId](#cfn-quicksight-analysis-cascadingcontrolsource-sourcesheetcontrolid): String
```

## Properties<a name="aws-properties-quicksight-analysis-cascadingcontrolsource-properties"></a>

`ColumnToMatch`  <a name="cfn-quicksight-analysis-cascadingcontrolsource-columntomatch"></a>
The column identifier that determines which column to look up for the source sheet control\.  
*Required*: No  
*Type*: [ColumnIdentifier](aws-properties-quicksight-analysis-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceSheetControlId`  <a name="cfn-quicksight-analysis-cascadingcontrolsource-sourcesheetcontrolid"></a>
The source sheet control ID of a `CascadingControlSource`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)