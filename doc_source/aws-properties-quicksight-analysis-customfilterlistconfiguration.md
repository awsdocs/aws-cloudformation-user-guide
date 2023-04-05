# AWS::QuickSight::Analysis CustomFilterListConfiguration<a name="aws-properties-quicksight-analysis-customfilterlistconfiguration"></a>

A list of custom filter values\.

## Syntax<a name="aws-properties-quicksight-analysis-customfilterlistconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-customfilterlistconfiguration-syntax.json"></a>

```
{
  "[CategoryValues](#cfn-quicksight-analysis-customfilterlistconfiguration-categoryvalues)" : [ String, ... ],
  "[MatchOperator](#cfn-quicksight-analysis-customfilterlistconfiguration-matchoperator)" : String,
  "[NullOption](#cfn-quicksight-analysis-customfilterlistconfiguration-nulloption)" : String,
  "[SelectAllOptions](#cfn-quicksight-analysis-customfilterlistconfiguration-selectalloptions)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-customfilterlistconfiguration-syntax.yaml"></a>

```
  [CategoryValues](#cfn-quicksight-analysis-customfilterlistconfiguration-categoryvalues): 
    - String
  [MatchOperator](#cfn-quicksight-analysis-customfilterlistconfiguration-matchoperator): String
  [NullOption](#cfn-quicksight-analysis-customfilterlistconfiguration-nulloption): String
  [SelectAllOptions](#cfn-quicksight-analysis-customfilterlistconfiguration-selectalloptions): String
```

## Properties<a name="aws-properties-quicksight-analysis-customfilterlistconfiguration-properties"></a>

`CategoryValues`  <a name="cfn-quicksight-analysis-customfilterlistconfiguration-categoryvalues"></a>
The list of category values for the filter\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchOperator`  <a name="cfn-quicksight-analysis-customfilterlistconfiguration-matchoperator"></a>
The match operator that is used to determine if a filter should be applied\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CONTAINS | DOES_NOT_CONTAIN | DOES_NOT_EQUAL | ENDS_WITH | EQUALS | STARTS_WITH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NullOption`  <a name="cfn-quicksight-analysis-customfilterlistconfiguration-nulloption"></a>
This option determines how null values should be treated when filtering data\.  
+  `ALL_VALUES`: Include null values in filtered results\.
+  `NULLS_ONLY`: Only include null values in filtered results\.
+  `NON_NULLS_ONLY`: Exclude null values from filtered results\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALL_VALUES | NON_NULLS_ONLY | NULLS_ONLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectAllOptions`  <a name="cfn-quicksight-analysis-customfilterlistconfiguration-selectalloptions"></a>
Select all of the values\. Null is not the assigned value of select all\.  
+  `FILTER_ALL_VALUES` 
*Required*: No  
*Type*: String  
*Allowed values*: `FILTER_ALL_VALUES`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)