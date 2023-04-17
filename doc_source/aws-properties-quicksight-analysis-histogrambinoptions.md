# AWS::QuickSight::Analysis HistogramBinOptions<a name="aws-properties-quicksight-analysis-histogrambinoptions"></a>

The options that determine the presentation of histogram bins\.

## Syntax<a name="aws-properties-quicksight-analysis-histogrambinoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-histogrambinoptions-syntax.json"></a>

```
{
  "[BinCount](#cfn-quicksight-analysis-histogrambinoptions-bincount)" : BinCountOptions,
  "[BinWidth](#cfn-quicksight-analysis-histogrambinoptions-binwidth)" : BinWidthOptions,
  "[SelectedBinType](#cfn-quicksight-analysis-histogrambinoptions-selectedbintype)" : String,
  "[StartValue](#cfn-quicksight-analysis-histogrambinoptions-startvalue)" : Double
}
```

### YAML<a name="aws-properties-quicksight-analysis-histogrambinoptions-syntax.yaml"></a>

```
  [BinCount](#cfn-quicksight-analysis-histogrambinoptions-bincount): 
    BinCountOptions
  [BinWidth](#cfn-quicksight-analysis-histogrambinoptions-binwidth): 
    BinWidthOptions
  [SelectedBinType](#cfn-quicksight-analysis-histogrambinoptions-selectedbintype): String
  [StartValue](#cfn-quicksight-analysis-histogrambinoptions-startvalue): Double
```

## Properties<a name="aws-properties-quicksight-analysis-histogrambinoptions-properties"></a>

`BinCount`  <a name="cfn-quicksight-analysis-histogrambinoptions-bincount"></a>
The options that determine the bin count of a histogram\.  
*Required*: No  
*Type*: [BinCountOptions](aws-properties-quicksight-analysis-bincountoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BinWidth`  <a name="cfn-quicksight-analysis-histogrambinoptions-binwidth"></a>
The options that determine the bin width of a histogram\.  
*Required*: No  
*Type*: [BinWidthOptions](aws-properties-quicksight-analysis-binwidthoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectedBinType`  <a name="cfn-quicksight-analysis-histogrambinoptions-selectedbintype"></a>
The options that determine the selected bin type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `BIN_COUNT | BIN_WIDTH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartValue`  <a name="cfn-quicksight-analysis-histogrambinoptions-startvalue"></a>
The options that determine the bin start value\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)