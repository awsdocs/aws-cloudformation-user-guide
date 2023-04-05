# AWS::QuickSight::Dashboard DrillDownFilter<a name="aws-properties-quicksight-dashboard-drilldownfilter"></a>

The drill down filter for the column hierarchies\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-drilldownfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-drilldownfilter-syntax.json"></a>

```
{
  "[CategoryFilter](#cfn-quicksight-dashboard-drilldownfilter-categoryfilter)" : CategoryDrillDownFilter,
  "[NumericEqualityFilter](#cfn-quicksight-dashboard-drilldownfilter-numericequalityfilter)" : NumericEqualityDrillDownFilter,
  "[TimeRangeFilter](#cfn-quicksight-dashboard-drilldownfilter-timerangefilter)" : TimeRangeDrillDownFilter
}
```

### YAML<a name="aws-properties-quicksight-dashboard-drilldownfilter-syntax.yaml"></a>

```
  [CategoryFilter](#cfn-quicksight-dashboard-drilldownfilter-categoryfilter): 
    CategoryDrillDownFilter
  [NumericEqualityFilter](#cfn-quicksight-dashboard-drilldownfilter-numericequalityfilter): 
    NumericEqualityDrillDownFilter
  [TimeRangeFilter](#cfn-quicksight-dashboard-drilldownfilter-timerangefilter): 
    TimeRangeDrillDownFilter
```

## Properties<a name="aws-properties-quicksight-dashboard-drilldownfilter-properties"></a>

`CategoryFilter`  <a name="cfn-quicksight-dashboard-drilldownfilter-categoryfilter"></a>
The category type drill down filter\. This filter is used for string type columns\.  
*Required*: No  
*Type*: [CategoryDrillDownFilter](aws-properties-quicksight-dashboard-categorydrilldownfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericEqualityFilter`  <a name="cfn-quicksight-dashboard-drilldownfilter-numericequalityfilter"></a>
The numeric equality type drill down filter\. This filter is used for number type columns\.  
*Required*: No  
*Type*: [NumericEqualityDrillDownFilter](aws-properties-quicksight-dashboard-numericequalitydrilldownfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeRangeFilter`  <a name="cfn-quicksight-dashboard-drilldownfilter-timerangefilter"></a>
The time range drill down filter\. This filter is used for date time columns\.  
*Required*: No  
*Type*: [TimeRangeDrillDownFilter](aws-properties-quicksight-dashboard-timerangedrilldownfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)