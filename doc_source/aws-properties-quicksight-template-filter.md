# AWS::QuickSight::Template Filter<a name="aws-properties-quicksight-template-filter"></a>

With a `Filter`, you can remove portions of data from a particular visual or view\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-filter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-filter-syntax.json"></a>

```
{
  "[CategoryFilter](#cfn-quicksight-template-filter-categoryfilter)" : CategoryFilter,
  "[NumericEqualityFilter](#cfn-quicksight-template-filter-numericequalityfilter)" : NumericEqualityFilter,
  "[NumericRangeFilter](#cfn-quicksight-template-filter-numericrangefilter)" : NumericRangeFilter,
  "[RelativeDatesFilter](#cfn-quicksight-template-filter-relativedatesfilter)" : RelativeDatesFilter,
  "[TimeEqualityFilter](#cfn-quicksight-template-filter-timeequalityfilter)" : TimeEqualityFilter,
  "[TimeRangeFilter](#cfn-quicksight-template-filter-timerangefilter)" : TimeRangeFilter,
  "[TopBottomFilter](#cfn-quicksight-template-filter-topbottomfilter)" : TopBottomFilter
}
```

### YAML<a name="aws-properties-quicksight-template-filter-syntax.yaml"></a>

```
  [CategoryFilter](#cfn-quicksight-template-filter-categoryfilter): 
    CategoryFilter
  [NumericEqualityFilter](#cfn-quicksight-template-filter-numericequalityfilter): 
    NumericEqualityFilter
  [NumericRangeFilter](#cfn-quicksight-template-filter-numericrangefilter): 
    NumericRangeFilter
  [RelativeDatesFilter](#cfn-quicksight-template-filter-relativedatesfilter): 
    RelativeDatesFilter
  [TimeEqualityFilter](#cfn-quicksight-template-filter-timeequalityfilter): 
    TimeEqualityFilter
  [TimeRangeFilter](#cfn-quicksight-template-filter-timerangefilter): 
    TimeRangeFilter
  [TopBottomFilter](#cfn-quicksight-template-filter-topbottomfilter): 
    TopBottomFilter
```

## Properties<a name="aws-properties-quicksight-template-filter-properties"></a>

`CategoryFilter`  <a name="cfn-quicksight-template-filter-categoryfilter"></a>
A `CategoryFilter` filters text values\.  
For more information, see [Adding text filters](https://docs.aws.amazon.com/quicksight/latest/user/add-a-text-filter-data-prep.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: [CategoryFilter](aws-properties-quicksight-template-categoryfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericEqualityFilter`  <a name="cfn-quicksight-template-filter-numericequalityfilter"></a>
A `NumericEqualityFilter` filters numeric values that equal or do not equal a given numeric value\.  
*Required*: No  
*Type*: [NumericEqualityFilter](aws-properties-quicksight-template-numericequalityfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericRangeFilter`  <a name="cfn-quicksight-template-filter-numericrangefilter"></a>
A `NumericRangeFilter` filters numeric values that are either inside or outside a given numeric range\.  
*Required*: No  
*Type*: [NumericRangeFilter](aws-properties-quicksight-template-numericrangefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelativeDatesFilter`  <a name="cfn-quicksight-template-filter-relativedatesfilter"></a>
A `RelativeDatesFilter` filters date values that are relative to a given date\.  
*Required*: No  
*Type*: [RelativeDatesFilter](aws-properties-quicksight-template-relativedatesfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeEqualityFilter`  <a name="cfn-quicksight-template-filter-timeequalityfilter"></a>
A `TimeEqualityFilter` filters date\-time values that equal or do not equal a given date/time value\.  
*Required*: No  
*Type*: [TimeEqualityFilter](aws-properties-quicksight-template-timeequalityfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeRangeFilter`  <a name="cfn-quicksight-template-filter-timerangefilter"></a>
A `TimeRangeFilter` filters date\-time values that are either inside or outside a given date/time range\.  
*Required*: No  
*Type*: [TimeRangeFilter](aws-properties-quicksight-template-timerangefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopBottomFilter`  <a name="cfn-quicksight-template-filter-topbottomfilter"></a>
A `TopBottomFilter` filters data to the top or bottom values for a given column\.  
*Required*: No  
*Type*: [TopBottomFilter](aws-properties-quicksight-template-topbottomfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)