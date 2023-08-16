# AWS::QuickSight::Analysis DateTimeHierarchy<a name="aws-properties-quicksight-analysis-datetimehierarchy"></a>

The option that determines the hierarchy of any `DateTime` fields\.

## Syntax<a name="aws-properties-quicksight-analysis-datetimehierarchy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-datetimehierarchy-syntax.json"></a>

```
{
  "[DrillDownFilters](#cfn-quicksight-analysis-datetimehierarchy-drilldownfilters)" : [ DrillDownFilter, ... ],
  "[HierarchyId](#cfn-quicksight-analysis-datetimehierarchy-hierarchyid)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-datetimehierarchy-syntax.yaml"></a>

```
  [DrillDownFilters](#cfn-quicksight-analysis-datetimehierarchy-drilldownfilters): 
    - DrillDownFilter
  [HierarchyId](#cfn-quicksight-analysis-datetimehierarchy-hierarchyid): String
```

## Properties<a name="aws-properties-quicksight-analysis-datetimehierarchy-properties"></a>

`DrillDownFilters`  <a name="cfn-quicksight-analysis-datetimehierarchy-drilldownfilters"></a>
The option that determines the drill down filters for the `DateTime` hierarchy\.  
*Required*: No  
*Type*: List of [DrillDownFilter](aws-properties-quicksight-analysis-drilldownfilter.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HierarchyId`  <a name="cfn-quicksight-analysis-datetimehierarchy-hierarchyid"></a>
The hierarchy ID of the `DateTime` hierarchy\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)