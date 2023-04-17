# AWS::QuickSight::Dashboard VisualSubtitleLabelOptions<a name="aws-properties-quicksight-dashboard-visualsubtitlelabeloptions"></a>

The subtitle label options for a visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-visualsubtitlelabeloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-visualsubtitlelabeloptions-syntax.json"></a>

```
{
  "[FormatText](#cfn-quicksight-dashboard-visualsubtitlelabeloptions-formattext)" : LongFormatText,
  "[Visibility](#cfn-quicksight-dashboard-visualsubtitlelabeloptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-visualsubtitlelabeloptions-syntax.yaml"></a>

```
  [FormatText](#cfn-quicksight-dashboard-visualsubtitlelabeloptions-formattext): 
    LongFormatText
  [Visibility](#cfn-quicksight-dashboard-visualsubtitlelabeloptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-visualsubtitlelabeloptions-properties"></a>

`FormatText`  <a name="cfn-quicksight-dashboard-visualsubtitlelabeloptions-formattext"></a>
The long text format of the subtitle label, such as plain text or rich text\.  
*Required*: No  
*Type*: [LongFormatText](aws-properties-quicksight-dashboard-longformattext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-dashboard-visualsubtitlelabeloptions-visibility"></a>
The visibility of the subtitle label\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)