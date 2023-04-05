# AWS::QuickSight::Template FontConfiguration<a name="aws-properties-quicksight-template-fontconfiguration"></a>

Configures the display properties of the given text\.

## Syntax<a name="aws-properties-quicksight-template-fontconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-fontconfiguration-syntax.json"></a>

```
{
  "[FontColor](#cfn-quicksight-template-fontconfiguration-fontcolor)" : String,
  "[FontDecoration](#cfn-quicksight-template-fontconfiguration-fontdecoration)" : String,
  "[FontSize](#cfn-quicksight-template-fontconfiguration-fontsize)" : FontSize,
  "[FontStyle](#cfn-quicksight-template-fontconfiguration-fontstyle)" : String,
  "[FontWeight](#cfn-quicksight-template-fontconfiguration-fontweight)" : FontWeight
}
```

### YAML<a name="aws-properties-quicksight-template-fontconfiguration-syntax.yaml"></a>

```
  [FontColor](#cfn-quicksight-template-fontconfiguration-fontcolor): String
  [FontDecoration](#cfn-quicksight-template-fontconfiguration-fontdecoration): String
  [FontSize](#cfn-quicksight-template-fontconfiguration-fontsize): 
    FontSize
  [FontStyle](#cfn-quicksight-template-fontconfiguration-fontstyle): String
  [FontWeight](#cfn-quicksight-template-fontconfiguration-fontweight): 
    FontWeight
```

## Properties<a name="aws-properties-quicksight-template-fontconfiguration-properties"></a>

`FontColor`  <a name="cfn-quicksight-template-fontconfiguration-fontcolor"></a>
Determines the color of the text\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontDecoration`  <a name="cfn-quicksight-template-fontconfiguration-fontdecoration"></a>
Determines the appearance of decorative lines on the text\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | UNDERLINE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontSize`  <a name="cfn-quicksight-template-fontconfiguration-fontsize"></a>
The option that determines the text display size\.  
*Required*: No  
*Type*: [FontSize](aws-properties-quicksight-template-fontsize.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontStyle`  <a name="cfn-quicksight-template-fontconfiguration-fontstyle"></a>
Determines the text display face that is inherited by the given font family\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ITALIC | NORMAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontWeight`  <a name="cfn-quicksight-template-fontconfiguration-fontweight"></a>
The option that determines the text display weight, or boldness\.  
*Required*: No  
*Type*: [FontWeight](aws-properties-quicksight-template-fontweight.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)