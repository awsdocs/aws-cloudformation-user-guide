# AWS::QuickSight::Template CustomFilterConfiguration<a name="aws-properties-quicksight-template-customfilterconfiguration"></a>

A custom filter that filters based on a single value\. This filter can be partially matched\.

## Syntax<a name="aws-properties-quicksight-template-customfilterconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-customfilterconfiguration-syntax.json"></a>

```
{
  "[CategoryValue](#cfn-quicksight-template-customfilterconfiguration-categoryvalue)" : String,
  "[MatchOperator](#cfn-quicksight-template-customfilterconfiguration-matchoperator)" : String,
  "[NullOption](#cfn-quicksight-template-customfilterconfiguration-nulloption)" : String,
  "[ParameterName](#cfn-quicksight-template-customfilterconfiguration-parametername)" : String,
  "[SelectAllOptions](#cfn-quicksight-template-customfilterconfiguration-selectalloptions)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-customfilterconfiguration-syntax.yaml"></a>

```
  [CategoryValue](#cfn-quicksight-template-customfilterconfiguration-categoryvalue): String
  [MatchOperator](#cfn-quicksight-template-customfilterconfiguration-matchoperator): String
  [NullOption](#cfn-quicksight-template-customfilterconfiguration-nulloption): String
  [ParameterName](#cfn-quicksight-template-customfilterconfiguration-parametername): String
  [SelectAllOptions](#cfn-quicksight-template-customfilterconfiguration-selectalloptions): String
```

## Properties<a name="aws-properties-quicksight-template-customfilterconfiguration-properties"></a>

`CategoryValue`  <a name="cfn-quicksight-template-customfilterconfiguration-categoryvalue"></a>
The category value for the filter\.  
This field is mutually exclusive to `ParameterName`\.  
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchOperator`  <a name="cfn-quicksight-template-customfilterconfiguration-matchoperator"></a>
The match operator that is used to determine if a filter should be applied\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CONTAINS | DOES_NOT_CONTAIN | DOES_NOT_EQUAL | ENDS_WITH | EQUALS | STARTS_WITH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NullOption`  <a name="cfn-quicksight-template-customfilterconfiguration-nulloption"></a>
This option determines how null values should be treated when filtering data\.  
+  `ALL_VALUES`: Include null values in filtered results\.
+  `NULLS_ONLY`: Only include null values in filtered results\.
+  `NON_NULLS_ONLY`: Exclude null values from filtered results\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALL_VALUES | NON_NULLS_ONLY | NULLS_ONLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterName`  <a name="cfn-quicksight-template-customfilterconfiguration-parametername"></a>
The parameter whose value should be used for the filter value\.  
This field is mutually exclusive to `CategoryValue`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectAllOptions`  <a name="cfn-quicksight-template-customfilterconfiguration-selectalloptions"></a>
Select all of the values\. Null is not the assigned value of select all\.  
+  `FILTER_ALL_VALUES` 
*Required*: No  
*Type*: String  
*Allowed values*: `FILTER_ALL_VALUES`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)