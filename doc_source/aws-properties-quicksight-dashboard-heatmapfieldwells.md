# AWS::QuickSight::Dashboard HeatMapFieldWells<a name="aws-properties-quicksight-dashboard-heatmapfieldwells"></a>

The field well configuration of a heat map\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-heatmapfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-heatmapfieldwells-syntax.json"></a>

```
{
  "[HeatMapAggregatedFieldWells](#cfn-quicksight-dashboard-heatmapfieldwells-heatmapaggregatedfieldwells)" : HeatMapAggregatedFieldWells
}
```

### YAML<a name="aws-properties-quicksight-dashboard-heatmapfieldwells-syntax.yaml"></a>

```
  [HeatMapAggregatedFieldWells](#cfn-quicksight-dashboard-heatmapfieldwells-heatmapaggregatedfieldwells): 
    HeatMapAggregatedFieldWells
```

## Properties<a name="aws-properties-quicksight-dashboard-heatmapfieldwells-properties"></a>

`HeatMapAggregatedFieldWells`  <a name="cfn-quicksight-dashboard-heatmapfieldwells-heatmapaggregatedfieldwells"></a>
The aggregated field wells of a heat map\.  
*Required*: No  
*Type*: [HeatMapAggregatedFieldWells](aws-properties-quicksight-dashboard-heatmapaggregatedfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)