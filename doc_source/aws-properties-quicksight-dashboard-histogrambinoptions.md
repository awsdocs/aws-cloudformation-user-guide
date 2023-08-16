# AWS::QuickSight::Dashboard HistogramBinOptions<a name="aws-properties-quicksight-dashboard-histogrambinoptions"></a>

The options that determine the presentation of histogram bins\.

## Syntax<a name="aws-properties-quicksight-dashboard-histogrambinoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-histogrambinoptions-syntax.json"></a>

```
{
  "[BinCount](#cfn-quicksight-dashboard-histogrambinoptions-bincount)" : BinCountOptions,
  "[BinWidth](#cfn-quicksight-dashboard-histogrambinoptions-binwidth)" : BinWidthOptions,
  "[SelectedBinType](#cfn-quicksight-dashboard-histogrambinoptions-selectedbintype)" : String,
  "[StartValue](#cfn-quicksight-dashboard-histogrambinoptions-startvalue)" : Double
}
```

### YAML<a name="aws-properties-quicksight-dashboard-histogrambinoptions-syntax.yaml"></a>

```
  [BinCount](#cfn-quicksight-dashboard-histogrambinoptions-bincount): 
    BinCountOptions
  [BinWidth](#cfn-quicksight-dashboard-histogrambinoptions-binwidth): 
    BinWidthOptions
  [SelectedBinType](#cfn-quicksight-dashboard-histogrambinoptions-selectedbintype): String
  [StartValue](#cfn-quicksight-dashboard-histogrambinoptions-startvalue): Double
```

## Properties<a name="aws-properties-quicksight-dashboard-histogrambinoptions-properties"></a>

`BinCount`  <a name="cfn-quicksight-dashboard-histogrambinoptions-bincount"></a>
The options that determine the bin count of a histogram\.  
*Required*: No  
*Type*: [BinCountOptions](aws-properties-quicksight-dashboard-bincountoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BinWidth`  <a name="cfn-quicksight-dashboard-histogrambinoptions-binwidth"></a>
The options that determine the bin width of a histogram\.  
*Required*: No  
*Type*: [BinWidthOptions](aws-properties-quicksight-dashboard-binwidthoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectedBinType`  <a name="cfn-quicksight-dashboard-histogrambinoptions-selectedbintype"></a>
The options that determine the selected bin type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `BIN_COUNT | BIN_WIDTH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartValue`  <a name="cfn-quicksight-dashboard-histogrambinoptions-startvalue"></a>
The options that determine the bin start value\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)