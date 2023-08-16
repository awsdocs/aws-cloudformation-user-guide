# AWS::QuickSight::Analysis CategoryFilter<a name="aws-properties-quicksight-analysis-categoryfilter"></a>

A `CategoryFilter` filters text values\.

For more information, see [Adding text filters](https://docs.aws.amazon.com/quicksight/latest/user/add-a-text-filter-data-prep.html) in the *Amazon QuickSight User Guide*\.

## Syntax<a name="aws-properties-quicksight-analysis-categoryfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-categoryfilter-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-analysis-categoryfilter-column)" : ColumnIdentifier,
  "[Configuration](#cfn-quicksight-analysis-categoryfilter-configuration)" : CategoryFilterConfiguration,
  "[FilterId](#cfn-quicksight-analysis-categoryfilter-filterid)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-categoryfilter-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-analysis-categoryfilter-column): 
    ColumnIdentifier
  [Configuration](#cfn-quicksight-analysis-categoryfilter-configuration): 
    CategoryFilterConfiguration
  [FilterId](#cfn-quicksight-analysis-categoryfilter-filterid): String
```

## Properties<a name="aws-properties-quicksight-analysis-categoryfilter-properties"></a>

`Column`  <a name="cfn-quicksight-analysis-categoryfilter-column"></a>
The column that the filter is applied to\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-analysis-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Configuration`  <a name="cfn-quicksight-analysis-categoryfilter-configuration"></a>
The configuration for a `CategoryFilter`\.  
*Required*: Yes  
*Type*: [CategoryFilterConfiguration](aws-properties-quicksight-analysis-categoryfilterconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterId`  <a name="cfn-quicksight-analysis-categoryfilter-filterid"></a>
An identifier that uniquely identifies a filter within a dashboard, analysis, or template\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)