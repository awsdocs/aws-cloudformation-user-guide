# AWS::QuickSight::Analysis VisualSubtitleLabelOptions<a name="aws-properties-quicksight-analysis-visualsubtitlelabeloptions"></a>

The subtitle label options for a visual\.

## Syntax<a name="aws-properties-quicksight-analysis-visualsubtitlelabeloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-visualsubtitlelabeloptions-syntax.json"></a>

```
{
  "[FormatText](#cfn-quicksight-analysis-visualsubtitlelabeloptions-formattext)" : LongFormatText,
  "[Visibility](#cfn-quicksight-analysis-visualsubtitlelabeloptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-visualsubtitlelabeloptions-syntax.yaml"></a>

```
  [FormatText](#cfn-quicksight-analysis-visualsubtitlelabeloptions-formattext): 
    LongFormatText
  [Visibility](#cfn-quicksight-analysis-visualsubtitlelabeloptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-analysis-visualsubtitlelabeloptions-properties"></a>

`FormatText`  <a name="cfn-quicksight-analysis-visualsubtitlelabeloptions-formattext"></a>
The long text format of the subtitle label, such as plain text or rich text\.  
*Required*: No  
*Type*: [LongFormatText](aws-properties-quicksight-analysis-longformattext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-analysis-visualsubtitlelabeloptions-visibility"></a>
The visibility of the subtitle label\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)