# AWS::QuickSight::Dashboard VisualTitleLabelOptions<a name="aws-properties-quicksight-dashboard-visualtitlelabeloptions"></a>

The title label options for a visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-visualtitlelabeloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-visualtitlelabeloptions-syntax.json"></a>

```
{
  "[FormatText](#cfn-quicksight-dashboard-visualtitlelabeloptions-formattext)" : ShortFormatText,
  "[Visibility](#cfn-quicksight-dashboard-visualtitlelabeloptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-visualtitlelabeloptions-syntax.yaml"></a>

```
  [FormatText](#cfn-quicksight-dashboard-visualtitlelabeloptions-formattext): 
    ShortFormatText
  [Visibility](#cfn-quicksight-dashboard-visualtitlelabeloptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-visualtitlelabeloptions-properties"></a>

`FormatText`  <a name="cfn-quicksight-dashboard-visualtitlelabeloptions-formattext"></a>
The short text format of the title label, such as plain text or rich text\.  
*Required*: No  
*Type*: [ShortFormatText](aws-properties-quicksight-dashboard-shortformattext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-dashboard-visualtitlelabeloptions-visibility"></a>
The visibility of the title label\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)