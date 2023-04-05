# AWS::QuickSight::Template TreeMapAggregatedFieldWells<a name="aws-properties-quicksight-template-treemapaggregatedfieldwells"></a>

Aggregated field wells of a tree map\.

## Syntax<a name="aws-properties-quicksight-template-treemapaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-treemapaggregatedfieldwells-syntax.json"></a>

```
{
  "[Colors](#cfn-quicksight-template-treemapaggregatedfieldwells-colors)" : [ MeasureField, ... ],
  "[Groups](#cfn-quicksight-template-treemapaggregatedfieldwells-groups)" : [ DimensionField, ... ],
  "[Sizes](#cfn-quicksight-template-treemapaggregatedfieldwells-sizes)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-treemapaggregatedfieldwells-syntax.yaml"></a>

```
  [Colors](#cfn-quicksight-template-treemapaggregatedfieldwells-colors): 
    - MeasureField
  [Groups](#cfn-quicksight-template-treemapaggregatedfieldwells-groups): 
    - DimensionField
  [Sizes](#cfn-quicksight-template-treemapaggregatedfieldwells-sizes): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-template-treemapaggregatedfieldwells-properties"></a>

`Colors`  <a name="cfn-quicksight-template-treemapaggregatedfieldwells-colors"></a>
The color field well of a tree map\. Values are grouped by aggregations based on group by fields\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Groups`  <a name="cfn-quicksight-template-treemapaggregatedfieldwells-groups"></a>
The group by field well of a tree map\. Values are grouped based on group by fields\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sizes`  <a name="cfn-quicksight-template-treemapaggregatedfieldwells-sizes"></a>
The size field well of a tree map\. Values are aggregated based on group by fields\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)