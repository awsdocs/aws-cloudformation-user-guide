# AWS::QuickSight::Analysis SecondaryValueOptions<a name="aws-properties-quicksight-analysis-secondaryvalueoptions"></a>

The options that determine the presentation of the secondary value of a KPI visual\.

## Syntax<a name="aws-properties-quicksight-analysis-secondaryvalueoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-secondaryvalueoptions-syntax.json"></a>

```
{
  "[Visibility](#cfn-quicksight-analysis-secondaryvalueoptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-secondaryvalueoptions-syntax.yaml"></a>

```
  [Visibility](#cfn-quicksight-analysis-secondaryvalueoptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-analysis-secondaryvalueoptions-properties"></a>

`Visibility`  <a name="cfn-quicksight-analysis-secondaryvalueoptions-visibility"></a>
Determines the visibility of the secondary value\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)