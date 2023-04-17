# AWS::QuickSight::Dashboard FontConfiguration<a name="aws-properties-quicksight-dashboard-fontconfiguration"></a>

Configures the display properties of the given text\.

## Syntax<a name="aws-properties-quicksight-dashboard-fontconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-fontconfiguration-syntax.json"></a>

```
{
  "[FontColor](#cfn-quicksight-dashboard-fontconfiguration-fontcolor)" : String,
  "[FontDecoration](#cfn-quicksight-dashboard-fontconfiguration-fontdecoration)" : String,
  "[FontSize](#cfn-quicksight-dashboard-fontconfiguration-fontsize)" : FontSize,
  "[FontStyle](#cfn-quicksight-dashboard-fontconfiguration-fontstyle)" : String,
  "[FontWeight](#cfn-quicksight-dashboard-fontconfiguration-fontweight)" : FontWeight
}
```

### YAML<a name="aws-properties-quicksight-dashboard-fontconfiguration-syntax.yaml"></a>

```
  [FontColor](#cfn-quicksight-dashboard-fontconfiguration-fontcolor): String
  [FontDecoration](#cfn-quicksight-dashboard-fontconfiguration-fontdecoration): String
  [FontSize](#cfn-quicksight-dashboard-fontconfiguration-fontsize): 
    FontSize
  [FontStyle](#cfn-quicksight-dashboard-fontconfiguration-fontstyle): String
  [FontWeight](#cfn-quicksight-dashboard-fontconfiguration-fontweight): 
    FontWeight
```

## Properties<a name="aws-properties-quicksight-dashboard-fontconfiguration-properties"></a>

`FontColor`  <a name="cfn-quicksight-dashboard-fontconfiguration-fontcolor"></a>
Determines the color of the text\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontDecoration`  <a name="cfn-quicksight-dashboard-fontconfiguration-fontdecoration"></a>
Determines the appearance of decorative lines on the text\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | UNDERLINE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontSize`  <a name="cfn-quicksight-dashboard-fontconfiguration-fontsize"></a>
The option that determines the text display size\.  
*Required*: No  
*Type*: [FontSize](aws-properties-quicksight-dashboard-fontsize.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontStyle`  <a name="cfn-quicksight-dashboard-fontconfiguration-fontstyle"></a>
Determines the text display face that is inherited by the given font family\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ITALIC | NORMAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontWeight`  <a name="cfn-quicksight-dashboard-fontconfiguration-fontweight"></a>
The option that determines the text display weight, or boldness\.  
*Required*: No  
*Type*: [FontWeight](aws-properties-quicksight-dashboard-fontweight.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)