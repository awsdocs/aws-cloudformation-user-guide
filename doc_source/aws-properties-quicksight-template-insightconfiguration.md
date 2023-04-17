# AWS::QuickSight::Template InsightConfiguration<a name="aws-properties-quicksight-template-insightconfiguration"></a>

The configuration of an insight visual\.

## Syntax<a name="aws-properties-quicksight-template-insightconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-insightconfiguration-syntax.json"></a>

```
{
  "[Computations](#cfn-quicksight-template-insightconfiguration-computations)" : [ Computation, ... ],
  "[CustomNarrative](#cfn-quicksight-template-insightconfiguration-customnarrative)" : CustomNarrativeOptions
}
```

### YAML<a name="aws-properties-quicksight-template-insightconfiguration-syntax.yaml"></a>

```
  [Computations](#cfn-quicksight-template-insightconfiguration-computations): 
    - Computation
  [CustomNarrative](#cfn-quicksight-template-insightconfiguration-customnarrative): 
    CustomNarrativeOptions
```

## Properties<a name="aws-properties-quicksight-template-insightconfiguration-properties"></a>

`Computations`  <a name="cfn-quicksight-template-insightconfiguration-computations"></a>
The computations configurations of the insight visual  
*Required*: No  
*Type*: List of [Computation](aws-properties-quicksight-template-computation.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomNarrative`  <a name="cfn-quicksight-template-insightconfiguration-customnarrative"></a>
The custom narrative of the insight visual\.  
*Required*: No  
*Type*: [CustomNarrativeOptions](aws-properties-quicksight-template-customnarrativeoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)