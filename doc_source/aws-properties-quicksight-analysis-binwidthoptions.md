# AWS::QuickSight::Analysis BinWidthOptions<a name="aws-properties-quicksight-analysis-binwidthoptions"></a>

The options that determine the bin width of a histogram\.

## Syntax<a name="aws-properties-quicksight-analysis-binwidthoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-binwidthoptions-syntax.json"></a>

```
{
  "[BinCountLimit](#cfn-quicksight-analysis-binwidthoptions-bincountlimit)" : Double,
  "[Value](#cfn-quicksight-analysis-binwidthoptions-value)" : Double
}
```

### YAML<a name="aws-properties-quicksight-analysis-binwidthoptions-syntax.yaml"></a>

```
  [BinCountLimit](#cfn-quicksight-analysis-binwidthoptions-bincountlimit): Double
  [Value](#cfn-quicksight-analysis-binwidthoptions-value): Double
```

## Properties<a name="aws-properties-quicksight-analysis-binwidthoptions-properties"></a>

`BinCountLimit`  <a name="cfn-quicksight-analysis-binwidthoptions-bincountlimit"></a>
The options that determine the bin count limit\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-analysis-binwidthoptions-value"></a>
The options that determine the bin width value\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)