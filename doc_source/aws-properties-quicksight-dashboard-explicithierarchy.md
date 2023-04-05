# AWS::QuickSight::Dashboard ExplicitHierarchy<a name="aws-properties-quicksight-dashboard-explicithierarchy"></a>

The option that determines the hierarchy of the fields that are built within a visual's field wells\. These fields can't be duplicated to other visuals\.

## Syntax<a name="aws-properties-quicksight-dashboard-explicithierarchy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-explicithierarchy-syntax.json"></a>

```
{
  "[Columns](#cfn-quicksight-dashboard-explicithierarchy-columns)" : [ ColumnIdentifier, ... ],
  "[DrillDownFilters](#cfn-quicksight-dashboard-explicithierarchy-drilldownfilters)" : [ DrillDownFilter, ... ],
  "[HierarchyId](#cfn-quicksight-dashboard-explicithierarchy-hierarchyid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-explicithierarchy-syntax.yaml"></a>

```
  [Columns](#cfn-quicksight-dashboard-explicithierarchy-columns): 
    - ColumnIdentifier
  [DrillDownFilters](#cfn-quicksight-dashboard-explicithierarchy-drilldownfilters): 
    - DrillDownFilter
  [HierarchyId](#cfn-quicksight-dashboard-explicithierarchy-hierarchyid): String
```

## Properties<a name="aws-properties-quicksight-dashboard-explicithierarchy-properties"></a>

`Columns`  <a name="cfn-quicksight-dashboard-explicithierarchy-columns"></a>
The list of columns that define the explicit hierarchy\.  
*Required*: Yes  
*Type*: List of [ColumnIdentifier](aws-properties-quicksight-dashboard-columnidentifier.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DrillDownFilters`  <a name="cfn-quicksight-dashboard-explicithierarchy-drilldownfilters"></a>
The option that determines the drill down filters for the explicit hierarchy\.  
*Required*: No  
*Type*: List of [DrillDownFilter](aws-properties-quicksight-dashboard-drilldownfilter.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HierarchyId`  <a name="cfn-quicksight-dashboard-explicithierarchy-hierarchyid"></a>
The hierarchy ID of the explicit hierarchy\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)