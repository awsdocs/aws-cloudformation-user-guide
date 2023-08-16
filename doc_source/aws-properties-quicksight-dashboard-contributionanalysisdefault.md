# AWS::QuickSight::Dashboard ContributionAnalysisDefault<a name="aws-properties-quicksight-dashboard-contributionanalysisdefault"></a>

The contribution analysis visual display for a line, pie, or bar chart\.

## Syntax<a name="aws-properties-quicksight-dashboard-contributionanalysisdefault-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-contributionanalysisdefault-syntax.json"></a>

```
{
  "[ContributorDimensions](#cfn-quicksight-dashboard-contributionanalysisdefault-contributordimensions)" : [ ColumnIdentifier, ... ],
  "[MeasureFieldId](#cfn-quicksight-dashboard-contributionanalysisdefault-measurefieldid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-contributionanalysisdefault-syntax.yaml"></a>

```
  [ContributorDimensions](#cfn-quicksight-dashboard-contributionanalysisdefault-contributordimensions): 
    - ColumnIdentifier
  [MeasureFieldId](#cfn-quicksight-dashboard-contributionanalysisdefault-measurefieldid): String
```

## Properties<a name="aws-properties-quicksight-dashboard-contributionanalysisdefault-properties"></a>

`ContributorDimensions`  <a name="cfn-quicksight-dashboard-contributionanalysisdefault-contributordimensions"></a>
The dimensions columns that are used in the contribution analysis, usually a list of `ColumnIdentifiers`\.  
*Required*: Yes  
*Type*: List of [ColumnIdentifier](aws-properties-quicksight-dashboard-columnidentifier.md)  
*Maximum*: `4`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MeasureFieldId`  <a name="cfn-quicksight-dashboard-contributionanalysisdefault-measurefieldid"></a>
The measure field that is used in the contribution analysis\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)