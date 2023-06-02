# AWS::QuickSight::DataSet LookbackWindow<a name="aws-properties-quicksight-dataset-lookbackwindow"></a>

The lookback window setup of an incremental refresh configuration\.

## Syntax<a name="aws-properties-quicksight-dataset-lookbackwindow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-lookbackwindow-syntax.json"></a>

```
{
  "[ColumnName](#cfn-quicksight-dataset-lookbackwindow-columnname)" : String,
  "[Size](#cfn-quicksight-dataset-lookbackwindow-size)" : Double,
  "[SizeUnit](#cfn-quicksight-dataset-lookbackwindow-sizeunit)" : String
}
```

### YAML<a name="aws-properties-quicksight-dataset-lookbackwindow-syntax.yaml"></a>

```
  [ColumnName](#cfn-quicksight-dataset-lookbackwindow-columnname): String
  [Size](#cfn-quicksight-dataset-lookbackwindow-size): Double
  [SizeUnit](#cfn-quicksight-dataset-lookbackwindow-sizeunit): String
```

## Properties<a name="aws-properties-quicksight-dataset-lookbackwindow-properties"></a>

`ColumnName`  <a name="cfn-quicksight-dataset-lookbackwindow-columnname"></a>
The name of the lookback window column\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-quicksight-dataset-lookbackwindow-size"></a>
The lookback window column size\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizeUnit`  <a name="cfn-quicksight-dataset-lookbackwindow-sizeunit"></a>
The size unit that is used for the lookback window column\. Valid values for this structure are `HOUR`, `DAY`, and `WEEK`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DAY | HOUR | WEEK`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)