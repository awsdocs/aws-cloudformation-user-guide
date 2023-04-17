# AWS::QuickSight::Template SankeyDiagramAggregatedFieldWells<a name="aws-properties-quicksight-template-sankeydiagramaggregatedfieldwells"></a>

The field well configuration of a sankey diagram\.

## Syntax<a name="aws-properties-quicksight-template-sankeydiagramaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-sankeydiagramaggregatedfieldwells-syntax.json"></a>

```
{
  "[Destination](#cfn-quicksight-template-sankeydiagramaggregatedfieldwells-destination)" : [ DimensionField, ... ],
  "[Source](#cfn-quicksight-template-sankeydiagramaggregatedfieldwells-source)" : [ DimensionField, ... ],
  "[Weight](#cfn-quicksight-template-sankeydiagramaggregatedfieldwells-weight)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-sankeydiagramaggregatedfieldwells-syntax.yaml"></a>

```
  [Destination](#cfn-quicksight-template-sankeydiagramaggregatedfieldwells-destination): 
    - DimensionField
  [Source](#cfn-quicksight-template-sankeydiagramaggregatedfieldwells-source): 
    - DimensionField
  [Weight](#cfn-quicksight-template-sankeydiagramaggregatedfieldwells-weight): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-template-sankeydiagramaggregatedfieldwells-properties"></a>

`Destination`  <a name="cfn-quicksight-template-sankeydiagramaggregatedfieldwells-destination"></a>
The destination field wells of a sankey diagram\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source`  <a name="cfn-quicksight-template-sankeydiagramaggregatedfieldwells-source"></a>
The source field wells of a sankey diagram\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Weight`  <a name="cfn-quicksight-template-sankeydiagramaggregatedfieldwells-weight"></a>
The weight field wells of a sankey diagram\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)