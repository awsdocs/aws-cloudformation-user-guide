# AWS::QuickSight::Analysis SankeyDiagramAggregatedFieldWells<a name="aws-properties-quicksight-analysis-sankeydiagramaggregatedfieldwells"></a>

The field well configuration of a sankey diagram\.

## Syntax<a name="aws-properties-quicksight-analysis-sankeydiagramaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-sankeydiagramaggregatedfieldwells-syntax.json"></a>

```
{
  "[Destination](#cfn-quicksight-analysis-sankeydiagramaggregatedfieldwells-destination)" : [ DimensionField, ... ],
  "[Source](#cfn-quicksight-analysis-sankeydiagramaggregatedfieldwells-source)" : [ DimensionField, ... ],
  "[Weight](#cfn-quicksight-analysis-sankeydiagramaggregatedfieldwells-weight)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-sankeydiagramaggregatedfieldwells-syntax.yaml"></a>

```
  [Destination](#cfn-quicksight-analysis-sankeydiagramaggregatedfieldwells-destination): 
    - DimensionField
  [Source](#cfn-quicksight-analysis-sankeydiagramaggregatedfieldwells-source): 
    - DimensionField
  [Weight](#cfn-quicksight-analysis-sankeydiagramaggregatedfieldwells-weight): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-analysis-sankeydiagramaggregatedfieldwells-properties"></a>

`Destination`  <a name="cfn-quicksight-analysis-sankeydiagramaggregatedfieldwells-destination"></a>
The destination field wells of a sankey diagram\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source`  <a name="cfn-quicksight-analysis-sankeydiagramaggregatedfieldwells-source"></a>
The source field wells of a sankey diagram\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Weight`  <a name="cfn-quicksight-analysis-sankeydiagramaggregatedfieldwells-weight"></a>
The weight field wells of a sankey diagram\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)