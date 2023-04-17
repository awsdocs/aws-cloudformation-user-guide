# AWS::QuickSight::Template DrillDownFilter<a name="aws-properties-quicksight-template-drilldownfilter"></a>

The drill down filter for the column hierarchies\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-drilldownfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-drilldownfilter-syntax.json"></a>

```
{
  "[CategoryFilter](#cfn-quicksight-template-drilldownfilter-categoryfilter)" : CategoryDrillDownFilter,
  "[NumericEqualityFilter](#cfn-quicksight-template-drilldownfilter-numericequalityfilter)" : NumericEqualityDrillDownFilter,
  "[TimeRangeFilter](#cfn-quicksight-template-drilldownfilter-timerangefilter)" : TimeRangeDrillDownFilter
}
```

### YAML<a name="aws-properties-quicksight-template-drilldownfilter-syntax.yaml"></a>

```
  [CategoryFilter](#cfn-quicksight-template-drilldownfilter-categoryfilter): 
    CategoryDrillDownFilter
  [NumericEqualityFilter](#cfn-quicksight-template-drilldownfilter-numericequalityfilter): 
    NumericEqualityDrillDownFilter
  [TimeRangeFilter](#cfn-quicksight-template-drilldownfilter-timerangefilter): 
    TimeRangeDrillDownFilter
```

## Properties<a name="aws-properties-quicksight-template-drilldownfilter-properties"></a>

`CategoryFilter`  <a name="cfn-quicksight-template-drilldownfilter-categoryfilter"></a>
The category type drill down filter\. This filter is used for string type columns\.  
*Required*: No  
*Type*: [CategoryDrillDownFilter](aws-properties-quicksight-template-categorydrilldownfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericEqualityFilter`  <a name="cfn-quicksight-template-drilldownfilter-numericequalityfilter"></a>
The numeric equality type drill down filter\. This filter is used for number type columns\.  
*Required*: No  
*Type*: [NumericEqualityDrillDownFilter](aws-properties-quicksight-template-numericequalitydrilldownfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeRangeFilter`  <a name="cfn-quicksight-template-drilldownfilter-timerangefilter"></a>
The time range drill down filter\. This filter is used for date time columns\.  
*Required*: No  
*Type*: [TimeRangeDrillDownFilter](aws-properties-quicksight-template-timerangedrilldownfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)