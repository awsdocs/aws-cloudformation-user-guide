# AWS::QuickSight::Dashboard TreeMapSortConfiguration<a name="aws-properties-quicksight-dashboard-treemapsortconfiguration"></a>

The sort configuration of a tree map\.

## Syntax<a name="aws-properties-quicksight-dashboard-treemapsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-treemapsortconfiguration-syntax.json"></a>

```
{
  "[TreeMapGroupItemsLimitConfiguration](#cfn-quicksight-dashboard-treemapsortconfiguration-treemapgroupitemslimitconfiguration)" : ItemsLimitConfiguration,
  "[TreeMapSort](#cfn-quicksight-dashboard-treemapsortconfiguration-treemapsort)" : [ FieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-treemapsortconfiguration-syntax.yaml"></a>

```
  [TreeMapGroupItemsLimitConfiguration](#cfn-quicksight-dashboard-treemapsortconfiguration-treemapgroupitemslimitconfiguration): 
    ItemsLimitConfiguration
  [TreeMapSort](#cfn-quicksight-dashboard-treemapsortconfiguration-treemapsort): 
    - FieldSortOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-treemapsortconfiguration-properties"></a>

`TreeMapGroupItemsLimitConfiguration`  <a name="cfn-quicksight-dashboard-treemapsortconfiguration-treemapgroupitemslimitconfiguration"></a>
The limit on the number of groups that are displayed\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-dashboard-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TreeMapSort`  <a name="cfn-quicksight-dashboard-treemapsortconfiguration-treemapsort"></a>
The sort configuration of group by fields\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-dashboard-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)