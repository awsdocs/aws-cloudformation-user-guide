# AWS::QuickSight::Dashboard FilledMapSortConfiguration<a name="aws-properties-quicksight-dashboard-filledmapsortconfiguration"></a>

The sort configuration of a `FilledMapVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-filledmapsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-filledmapsortconfiguration-syntax.json"></a>

```
{
  "[CategorySort](#cfn-quicksight-dashboard-filledmapsortconfiguration-categorysort)" : [ FieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-filledmapsortconfiguration-syntax.yaml"></a>

```
  [CategorySort](#cfn-quicksight-dashboard-filledmapsortconfiguration-categorysort): 
    - FieldSortOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-filledmapsortconfiguration-properties"></a>

`CategorySort`  <a name="cfn-quicksight-dashboard-filledmapsortconfiguration-categorysort"></a>
The sort configuration of the location fields\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-dashboard-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)