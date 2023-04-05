# AWS::QuickSight::Dashboard KPISortConfiguration<a name="aws-properties-quicksight-dashboard-kpisortconfiguration"></a>

The sort configuration of a KPI visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-kpisortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-kpisortconfiguration-syntax.json"></a>

```
{
  "[TrendGroupSort](#cfn-quicksight-dashboard-kpisortconfiguration-trendgroupsort)" : [ FieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-kpisortconfiguration-syntax.yaml"></a>

```
  [TrendGroupSort](#cfn-quicksight-dashboard-kpisortconfiguration-trendgroupsort): 
    - FieldSortOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-kpisortconfiguration-properties"></a>

`TrendGroupSort`  <a name="cfn-quicksight-dashboard-kpisortconfiguration-trendgroupsort"></a>
The sort configuration of the trend group fields\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-dashboard-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)