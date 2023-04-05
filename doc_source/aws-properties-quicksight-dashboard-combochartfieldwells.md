# AWS::QuickSight::Dashboard ComboChartFieldWells<a name="aws-properties-quicksight-dashboard-combochartfieldwells"></a>

The field wells of the visual\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-combochartfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-combochartfieldwells-syntax.json"></a>

```
{
  "[ComboChartAggregatedFieldWells](#cfn-quicksight-dashboard-combochartfieldwells-combochartaggregatedfieldwells)" : ComboChartAggregatedFieldWells
}
```

### YAML<a name="aws-properties-quicksight-dashboard-combochartfieldwells-syntax.yaml"></a>

```
  [ComboChartAggregatedFieldWells](#cfn-quicksight-dashboard-combochartfieldwells-combochartaggregatedfieldwells): 
    ComboChartAggregatedFieldWells
```

## Properties<a name="aws-properties-quicksight-dashboard-combochartfieldwells-properties"></a>

`ComboChartAggregatedFieldWells`  <a name="cfn-quicksight-dashboard-combochartfieldwells-combochartaggregatedfieldwells"></a>
The aggregated field wells of a combo chart\. Combo charts only have aggregated field wells\. Columns in a combo chart are aggregated by category\.  
*Required*: No  
*Type*: [ComboChartAggregatedFieldWells](aws-properties-quicksight-dashboard-combochartaggregatedfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)