# AWS::QuickSight::Template TreeMapSortConfiguration<a name="aws-properties-quicksight-template-treemapsortconfiguration"></a>

The sort configuration of a tree map\.

## Syntax<a name="aws-properties-quicksight-template-treemapsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-treemapsortconfiguration-syntax.json"></a>

```
{
  "[TreeMapGroupItemsLimitConfiguration](#cfn-quicksight-template-treemapsortconfiguration-treemapgroupitemslimitconfiguration)" : ItemsLimitConfiguration,
  "[TreeMapSort](#cfn-quicksight-template-treemapsortconfiguration-treemapsort)" : [ FieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-treemapsortconfiguration-syntax.yaml"></a>

```
  [TreeMapGroupItemsLimitConfiguration](#cfn-quicksight-template-treemapsortconfiguration-treemapgroupitemslimitconfiguration): 
    ItemsLimitConfiguration
  [TreeMapSort](#cfn-quicksight-template-treemapsortconfiguration-treemapsort): 
    - FieldSortOptions
```

## Properties<a name="aws-properties-quicksight-template-treemapsortconfiguration-properties"></a>

`TreeMapGroupItemsLimitConfiguration`  <a name="cfn-quicksight-template-treemapsortconfiguration-treemapgroupitemslimitconfiguration"></a>
The limit on the number of groups that are displayed\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-template-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TreeMapSort`  <a name="cfn-quicksight-template-treemapsortconfiguration-treemapsort"></a>
The sort configuration of group by fields\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-template-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)