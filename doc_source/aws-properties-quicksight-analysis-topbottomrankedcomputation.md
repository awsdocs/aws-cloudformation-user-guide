# AWS::QuickSight::Analysis TopBottomRankedComputation<a name="aws-properties-quicksight-analysis-topbottomrankedcomputation"></a>

The top ranked and bottom ranked computation configuration\.

## Syntax<a name="aws-properties-quicksight-analysis-topbottomrankedcomputation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-topbottomrankedcomputation-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-analysis-topbottomrankedcomputation-category)" : DimensionField,
  "[ComputationId](#cfn-quicksight-analysis-topbottomrankedcomputation-computationid)" : String,
  "[Name](#cfn-quicksight-analysis-topbottomrankedcomputation-name)" : String,
  "[ResultSize](#cfn-quicksight-analysis-topbottomrankedcomputation-resultsize)" : Double,
  "[Type](#cfn-quicksight-analysis-topbottomrankedcomputation-type)" : String,
  "[Value](#cfn-quicksight-analysis-topbottomrankedcomputation-value)" : MeasureField
}
```

### YAML<a name="aws-properties-quicksight-analysis-topbottomrankedcomputation-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-analysis-topbottomrankedcomputation-category): 
    DimensionField
  [ComputationId](#cfn-quicksight-analysis-topbottomrankedcomputation-computationid): String
  [Name](#cfn-quicksight-analysis-topbottomrankedcomputation-name): String
  [ResultSize](#cfn-quicksight-analysis-topbottomrankedcomputation-resultsize): Double
  [Type](#cfn-quicksight-analysis-topbottomrankedcomputation-type): String
  [Value](#cfn-quicksight-analysis-topbottomrankedcomputation-value): 
    MeasureField
```

## Properties<a name="aws-properties-quicksight-analysis-topbottomrankedcomputation-properties"></a>

`Category`  <a name="cfn-quicksight-analysis-topbottomrankedcomputation-category"></a>
The category field that is used in a computation\.  
*Required*: Yes  
*Type*: [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComputationId`  <a name="cfn-quicksight-analysis-topbottomrankedcomputation-computationid"></a>
The ID for a computation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-analysis-topbottomrankedcomputation-name"></a>
The name of a computation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResultSize`  <a name="cfn-quicksight-analysis-topbottomrankedcomputation-resultsize"></a>
The result size of a top and bottom ranked computation\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-analysis-topbottomrankedcomputation-type"></a>
The computation type\. Choose one of the following options:  
+ TOP: A top ranked computation\.
+ BOTTOM: A bottom ranked computation\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `BOTTOM | TOP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-analysis-topbottomrankedcomputation-value"></a>
The value field that is used in a computation\.  
*Required*: No  
*Type*: [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)