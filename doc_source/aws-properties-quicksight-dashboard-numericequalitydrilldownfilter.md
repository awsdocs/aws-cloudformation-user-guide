# AWS::QuickSight::Dashboard NumericEqualityDrillDownFilter<a name="aws-properties-quicksight-dashboard-numericequalitydrilldownfilter"></a>

The category drill down filter\.

## Syntax<a name="aws-properties-quicksight-dashboard-numericequalitydrilldownfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-numericequalitydrilldownfilter-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-dashboard-numericequalitydrilldownfilter-column)" : ColumnIdentifier,
  "[Value](#cfn-quicksight-dashboard-numericequalitydrilldownfilter-value)" : Double
}
```

### YAML<a name="aws-properties-quicksight-dashboard-numericequalitydrilldownfilter-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-dashboard-numericequalitydrilldownfilter-column): 
    ColumnIdentifier
  [Value](#cfn-quicksight-dashboard-numericequalitydrilldownfilter-value): Double
```

## Properties<a name="aws-properties-quicksight-dashboard-numericequalitydrilldownfilter-properties"></a>

`Column`  <a name="cfn-quicksight-dashboard-numericequalitydrilldownfilter-column"></a>
The column that the filter is applied to\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-dashboard-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-dashboard-numericequalitydrilldownfilter-value"></a>
The value of the double input numeric drill down filter\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)