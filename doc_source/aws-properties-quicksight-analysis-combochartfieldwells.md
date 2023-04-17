# AWS::QuickSight::Analysis ComboChartFieldWells<a name="aws-properties-quicksight-analysis-combochartfieldwells"></a>

The field wells of the visual\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-combochartfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-combochartfieldwells-syntax.json"></a>

```
{
  "[ComboChartAggregatedFieldWells](#cfn-quicksight-analysis-combochartfieldwells-combochartaggregatedfieldwells)" : ComboChartAggregatedFieldWells
}
```

### YAML<a name="aws-properties-quicksight-analysis-combochartfieldwells-syntax.yaml"></a>

```
  [ComboChartAggregatedFieldWells](#cfn-quicksight-analysis-combochartfieldwells-combochartaggregatedfieldwells): 
    ComboChartAggregatedFieldWells
```

## Properties<a name="aws-properties-quicksight-analysis-combochartfieldwells-properties"></a>

`ComboChartAggregatedFieldWells`  <a name="cfn-quicksight-analysis-combochartfieldwells-combochartaggregatedfieldwells"></a>
The aggregated field wells of a combo chart\. Combo charts only have aggregated field wells\. Columns in a combo chart are aggregated by category\.  
*Required*: No  
*Type*: [ComboChartAggregatedFieldWells](aws-properties-quicksight-analysis-combochartaggregatedfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)