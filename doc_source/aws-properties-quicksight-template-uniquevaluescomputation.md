# AWS::QuickSight::Template UniqueValuesComputation<a name="aws-properties-quicksight-template-uniquevaluescomputation"></a>

The unique values computation configuration\.

## Syntax<a name="aws-properties-quicksight-template-uniquevaluescomputation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-uniquevaluescomputation-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-template-uniquevaluescomputation-category)" : DimensionField,
  "[ComputationId](#cfn-quicksight-template-uniquevaluescomputation-computationid)" : String,
  "[Name](#cfn-quicksight-template-uniquevaluescomputation-name)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-uniquevaluescomputation-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-template-uniquevaluescomputation-category): 
    DimensionField
  [ComputationId](#cfn-quicksight-template-uniquevaluescomputation-computationid): String
  [Name](#cfn-quicksight-template-uniquevaluescomputation-name): String
```

## Properties<a name="aws-properties-quicksight-template-uniquevaluescomputation-properties"></a>

`Category`  <a name="cfn-quicksight-template-uniquevaluescomputation-category"></a>
The category field that is used in a computation\.  
*Required*: No  
*Type*: [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComputationId`  <a name="cfn-quicksight-template-uniquevaluescomputation-computationid"></a>
The ID for a computation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-template-uniquevaluescomputation-name"></a>
The name of a computation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)