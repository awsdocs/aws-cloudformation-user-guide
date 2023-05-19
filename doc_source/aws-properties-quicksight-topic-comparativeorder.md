# AWS::QuickSight::Topic ComparativeOrder<a name="aws-properties-quicksight-topic-comparativeorder"></a>

The order in which data is displayed for the column when it's used in a comparative context\.

## Syntax<a name="aws-properties-quicksight-topic-comparativeorder-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-comparativeorder-syntax.json"></a>

```
{
  "[SpecifedOrder](#cfn-quicksight-topic-comparativeorder-specifedorder)" : [ String, ... ],
  "[TreatUndefinedSpecifiedValues](#cfn-quicksight-topic-comparativeorder-treatundefinedspecifiedvalues)" : String,
  "[UseOrdering](#cfn-quicksight-topic-comparativeorder-useordering)" : String
}
```

### YAML<a name="aws-properties-quicksight-topic-comparativeorder-syntax.yaml"></a>

```
  [SpecifedOrder](#cfn-quicksight-topic-comparativeorder-specifedorder): 
    - String
  [TreatUndefinedSpecifiedValues](#cfn-quicksight-topic-comparativeorder-treatundefinedspecifiedvalues): String
  [UseOrdering](#cfn-quicksight-topic-comparativeorder-useordering): String
```

## Properties<a name="aws-properties-quicksight-topic-comparativeorder-properties"></a>

`SpecifedOrder`  <a name="cfn-quicksight-topic-comparativeorder-specifedorder"></a>
The list of columns to be used in the ordering\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TreatUndefinedSpecifiedValues`  <a name="cfn-quicksight-topic-comparativeorder-treatundefinedspecifiedvalues"></a>
The treat of undefined specified values\. Valid values for this structure are `LEAST` and `MOST`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `LEAST | MOST`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseOrdering`  <a name="cfn-quicksight-topic-comparativeorder-useordering"></a>
The ordering type for a column\. Valid values for this structure are `GREATER_IS_BETTER`, `LESSER_IS_BETTER` and `SPECIFIED`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `GREATER_IS_BETTER | LESSER_IS_BETTER | SPECIFIED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)