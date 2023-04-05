# AWS::QuickSight::Analysis FilterListConfiguration<a name="aws-properties-quicksight-analysis-filterlistconfiguration"></a>

A list of filter configurations\.

## Syntax<a name="aws-properties-quicksight-analysis-filterlistconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-filterlistconfiguration-syntax.json"></a>

```
{
  "[CategoryValues](#cfn-quicksight-analysis-filterlistconfiguration-categoryvalues)" : [ String, ... ],
  "[MatchOperator](#cfn-quicksight-analysis-filterlistconfiguration-matchoperator)" : String,
  "[SelectAllOptions](#cfn-quicksight-analysis-filterlistconfiguration-selectalloptions)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-filterlistconfiguration-syntax.yaml"></a>

```
  [CategoryValues](#cfn-quicksight-analysis-filterlistconfiguration-categoryvalues): 
    - String
  [MatchOperator](#cfn-quicksight-analysis-filterlistconfiguration-matchoperator): String
  [SelectAllOptions](#cfn-quicksight-analysis-filterlistconfiguration-selectalloptions): String
```

## Properties<a name="aws-properties-quicksight-analysis-filterlistconfiguration-properties"></a>

`CategoryValues`  <a name="cfn-quicksight-analysis-filterlistconfiguration-categoryvalues"></a>
The list of category values for the filter\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchOperator`  <a name="cfn-quicksight-analysis-filterlistconfiguration-matchoperator"></a>
The match operator that is used to determine if a filter should be applied\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CONTAINS | DOES_NOT_CONTAIN | DOES_NOT_EQUAL | ENDS_WITH | EQUALS | STARTS_WITH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectAllOptions`  <a name="cfn-quicksight-analysis-filterlistconfiguration-selectalloptions"></a>
Select all of the values\. Null is not the assigned value of select all\.  
+  `FILTER_ALL_VALUES` 
*Required*: No  
*Type*: String  
*Allowed values*: `FILTER_ALL_VALUES`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)