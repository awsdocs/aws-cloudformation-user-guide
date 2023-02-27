# AWS::QuickSight::Theme ThemeConfiguration<a name="aws-properties-quicksight-theme-themeconfiguration"></a>

The theme configuration\. This configuration contains all of the display properties for a theme\.

## Syntax<a name="aws-properties-quicksight-theme-themeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-theme-themeconfiguration-syntax.json"></a>

```
{
  "[DataColorPalette](#cfn-quicksight-theme-themeconfiguration-datacolorpalette)" : DataColorPalette,
  "[Sheet](#cfn-quicksight-theme-themeconfiguration-sheet)" : SheetStyle,
  "[Typography](#cfn-quicksight-theme-themeconfiguration-typography)" : Typography,
  "[UIColorPalette](#cfn-quicksight-theme-themeconfiguration-uicolorpalette)" : UIColorPalette
}
```

### YAML<a name="aws-properties-quicksight-theme-themeconfiguration-syntax.yaml"></a>

```
  [DataColorPalette](#cfn-quicksight-theme-themeconfiguration-datacolorpalette): 
    DataColorPalette
  [Sheet](#cfn-quicksight-theme-themeconfiguration-sheet): 
    SheetStyle
  [Typography](#cfn-quicksight-theme-themeconfiguration-typography): 
    Typography
  [UIColorPalette](#cfn-quicksight-theme-themeconfiguration-uicolorpalette): 
    UIColorPalette
```

## Properties<a name="aws-properties-quicksight-theme-themeconfiguration-properties"></a>

`DataColorPalette`  <a name="cfn-quicksight-theme-themeconfiguration-datacolorpalette"></a>
Color properties that apply to chart data colors\.  
*Required*: No  
*Type*: [DataColorPalette](aws-properties-quicksight-theme-datacolorpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sheet`  <a name="cfn-quicksight-theme-themeconfiguration-sheet"></a>
Display options related to sheets\.  
*Required*: No  
*Type*: [SheetStyle](aws-properties-quicksight-theme-sheetstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Typography`  <a name="cfn-quicksight-theme-themeconfiguration-typography"></a>
Property description not available\.  
*Required*: No  
*Type*: [Typography](aws-properties-quicksight-theme-typography.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UIColorPalette`  <a name="cfn-quicksight-theme-themeconfiguration-uicolorpalette"></a>
Color properties that apply to the UI and to charts, excluding the colors that apply to data\.   
*Required*: No  
*Type*: [UIColorPalette](aws-properties-quicksight-theme-uicolorpalette.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)