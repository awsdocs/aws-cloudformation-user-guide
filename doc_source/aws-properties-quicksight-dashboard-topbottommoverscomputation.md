# AWS::QuickSight::Dashboard TopBottomMoversComputation<a name="aws-properties-quicksight-dashboard-topbottommoverscomputation"></a>

The top movers and bottom movers computation setup\.

## Syntax<a name="aws-properties-quicksight-dashboard-topbottommoverscomputation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-topbottommoverscomputation-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-dashboard-topbottommoverscomputation-category)" : DimensionField,
  "[ComputationId](#cfn-quicksight-dashboard-topbottommoverscomputation-computationid)" : String,
  "[MoverSize](#cfn-quicksight-dashboard-topbottommoverscomputation-moversize)" : Double,
  "[Name](#cfn-quicksight-dashboard-topbottommoverscomputation-name)" : String,
  "[SortOrder](#cfn-quicksight-dashboard-topbottommoverscomputation-sortorder)" : String,
  "[Time](#cfn-quicksight-dashboard-topbottommoverscomputation-time)" : DimensionField,
  "[Type](#cfn-quicksight-dashboard-topbottommoverscomputation-type)" : String,
  "[Value](#cfn-quicksight-dashboard-topbottommoverscomputation-value)" : MeasureField
}
```

### YAML<a name="aws-properties-quicksight-dashboard-topbottommoverscomputation-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-dashboard-topbottommoverscomputation-category): 
    DimensionField
  [ComputationId](#cfn-quicksight-dashboard-topbottommoverscomputation-computationid): String
  [MoverSize](#cfn-quicksight-dashboard-topbottommoverscomputation-moversize): Double
  [Name](#cfn-quicksight-dashboard-topbottommoverscomputation-name): String
  [SortOrder](#cfn-quicksight-dashboard-topbottommoverscomputation-sortorder): String
  [Time](#cfn-quicksight-dashboard-topbottommoverscomputation-time): 
    DimensionField
  [Type](#cfn-quicksight-dashboard-topbottommoverscomputation-type): String
  [Value](#cfn-quicksight-dashboard-topbottommoverscomputation-value): 
    MeasureField
```

## Properties<a name="aws-properties-quicksight-dashboard-topbottommoverscomputation-properties"></a>

`Category`  <a name="cfn-quicksight-dashboard-topbottommoverscomputation-category"></a>
The category field that is used in a computation\.  
*Required*: Yes  
*Type*: [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComputationId`  <a name="cfn-quicksight-dashboard-topbottommoverscomputation-computationid"></a>
The ID for a computation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MoverSize`  <a name="cfn-quicksight-dashboard-topbottommoverscomputation-moversize"></a>
The mover size setup of the top and bottom movers computation\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-dashboard-topbottommoverscomputation-name"></a>
The name of a computation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortOrder`  <a name="cfn-quicksight-dashboard-topbottommoverscomputation-sortorder"></a>
The sort order setup of the top and bottom movers computation\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ABSOLUTE_DIFFERENCE | PERCENT_DIFFERENCE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Time`  <a name="cfn-quicksight-dashboard-topbottommoverscomputation-time"></a>
The time field that is used in a computation\.  
*Required*: Yes  
*Type*: [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-dashboard-topbottommoverscomputation-type"></a>
The computation type\. Choose from the following options:  
+ TOP: Top movers computation\.
+ BOTTOM: Bottom movers computation\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `BOTTOM | TOP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-dashboard-topbottommoverscomputation-value"></a>
The value field that is used in a computation\.  
*Required*: No  
*Type*: [MeasureField](aws-properties-quicksight-dashboard-measurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)