# AWS::QuickSight::Dashboard BinWidthOptions<a name="aws-properties-quicksight-dashboard-binwidthoptions"></a>

The options that determine the bin width of a histogram\.

## Syntax<a name="aws-properties-quicksight-dashboard-binwidthoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-binwidthoptions-syntax.json"></a>

```
{
  "[BinCountLimit](#cfn-quicksight-dashboard-binwidthoptions-bincountlimit)" : Double,
  "[Value](#cfn-quicksight-dashboard-binwidthoptions-value)" : Double
}
```

### YAML<a name="aws-properties-quicksight-dashboard-binwidthoptions-syntax.yaml"></a>

```
  [BinCountLimit](#cfn-quicksight-dashboard-binwidthoptions-bincountlimit): Double
  [Value](#cfn-quicksight-dashboard-binwidthoptions-value): Double
```

## Properties<a name="aws-properties-quicksight-dashboard-binwidthoptions-properties"></a>

`BinCountLimit`  <a name="cfn-quicksight-dashboard-binwidthoptions-bincountlimit"></a>
The options that determine the bin count limit\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-dashboard-binwidthoptions-value"></a>
The options that determine the bin width value\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)