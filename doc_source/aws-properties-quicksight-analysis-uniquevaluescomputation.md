# AWS::QuickSight::Analysis UniqueValuesComputation<a name="aws-properties-quicksight-analysis-uniquevaluescomputation"></a>

The unique values computation configuration\.

## Syntax<a name="aws-properties-quicksight-analysis-uniquevaluescomputation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-uniquevaluescomputation-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-analysis-uniquevaluescomputation-category)" : DimensionField,
  "[ComputationId](#cfn-quicksight-analysis-uniquevaluescomputation-computationid)" : String,
  "[Name](#cfn-quicksight-analysis-uniquevaluescomputation-name)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-uniquevaluescomputation-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-analysis-uniquevaluescomputation-category): 
    DimensionField
  [ComputationId](#cfn-quicksight-analysis-uniquevaluescomputation-computationid): String
  [Name](#cfn-quicksight-analysis-uniquevaluescomputation-name): String
```

## Properties<a name="aws-properties-quicksight-analysis-uniquevaluescomputation-properties"></a>

`Category`  <a name="cfn-quicksight-analysis-uniquevaluescomputation-category"></a>
The category field that is used in a computation\.  
*Required*: Yes  
*Type*: [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComputationId`  <a name="cfn-quicksight-analysis-uniquevaluescomputation-computationid"></a>
The ID for a computation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-analysis-uniquevaluescomputation-name"></a>
The name of a computation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)