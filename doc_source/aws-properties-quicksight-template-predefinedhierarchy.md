# AWS::QuickSight::Template PredefinedHierarchy<a name="aws-properties-quicksight-template-predefinedhierarchy"></a>

The option that determines the hierarchy of the fields that are defined during data preparation\. These fields are available to use in any analysis that uses the data source\.

## Syntax<a name="aws-properties-quicksight-template-predefinedhierarchy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-predefinedhierarchy-syntax.json"></a>

```
{
  "[Columns](#cfn-quicksight-template-predefinedhierarchy-columns)" : [ ColumnIdentifier, ... ],
  "[DrillDownFilters](#cfn-quicksight-template-predefinedhierarchy-drilldownfilters)" : [ DrillDownFilter, ... ],
  "[HierarchyId](#cfn-quicksight-template-predefinedhierarchy-hierarchyid)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-predefinedhierarchy-syntax.yaml"></a>

```
  [Columns](#cfn-quicksight-template-predefinedhierarchy-columns): 
    - ColumnIdentifier
  [DrillDownFilters](#cfn-quicksight-template-predefinedhierarchy-drilldownfilters): 
    - DrillDownFilter
  [HierarchyId](#cfn-quicksight-template-predefinedhierarchy-hierarchyid): String
```

## Properties<a name="aws-properties-quicksight-template-predefinedhierarchy-properties"></a>

`Columns`  <a name="cfn-quicksight-template-predefinedhierarchy-columns"></a>
The list of columns that define the predefined hierarchy\.  
*Required*: Yes  
*Type*: List of [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DrillDownFilters`  <a name="cfn-quicksight-template-predefinedhierarchy-drilldownfilters"></a>
The option that determines the drill down filters for the predefined hierarchy\.  
*Required*: No  
*Type*: List of [DrillDownFilter](aws-properties-quicksight-template-drilldownfilter.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HierarchyId`  <a name="cfn-quicksight-template-predefinedhierarchy-hierarchyid"></a>
The hierarchy ID of the predefined hierarchy\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)