# AWS::QuickSight::Template KPISortConfiguration<a name="aws-properties-quicksight-template-kpisortconfiguration"></a>

The sort configuration of a KPI visual\.

## Syntax<a name="aws-properties-quicksight-template-kpisortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-kpisortconfiguration-syntax.json"></a>

```
{
  "[TrendGroupSort](#cfn-quicksight-template-kpisortconfiguration-trendgroupsort)" : [ FieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-kpisortconfiguration-syntax.yaml"></a>

```
  [TrendGroupSort](#cfn-quicksight-template-kpisortconfiguration-trendgroupsort): 
    - FieldSortOptions
```

## Properties<a name="aws-properties-quicksight-template-kpisortconfiguration-properties"></a>

`TrendGroupSort`  <a name="cfn-quicksight-template-kpisortconfiguration-trendgroupsort"></a>
The sort configuration of the trend group fields\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-template-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)