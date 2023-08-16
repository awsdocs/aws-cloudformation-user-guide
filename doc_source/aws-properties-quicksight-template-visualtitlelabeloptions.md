# AWS::QuickSight::Template VisualTitleLabelOptions<a name="aws-properties-quicksight-template-visualtitlelabeloptions"></a>

The title label options for a visual\.

## Syntax<a name="aws-properties-quicksight-template-visualtitlelabeloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-visualtitlelabeloptions-syntax.json"></a>

```
{
  "[FormatText](#cfn-quicksight-template-visualtitlelabeloptions-formattext)" : ShortFormatText,
  "[Visibility](#cfn-quicksight-template-visualtitlelabeloptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-visualtitlelabeloptions-syntax.yaml"></a>

```
  [FormatText](#cfn-quicksight-template-visualtitlelabeloptions-formattext): 
    ShortFormatText
  [Visibility](#cfn-quicksight-template-visualtitlelabeloptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-template-visualtitlelabeloptions-properties"></a>

`FormatText`  <a name="cfn-quicksight-template-visualtitlelabeloptions-formattext"></a>
The short text format of the title label, such as plain text or rich text\.  
*Required*: No  
*Type*: [ShortFormatText](aws-properties-quicksight-template-shortformattext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-template-visualtitlelabeloptions-visibility"></a>
The visibility of the title label\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)