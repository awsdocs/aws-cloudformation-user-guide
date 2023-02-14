# AWS::QuickSight::Theme UIColorPalette<a name="aws-properties-quicksight-theme-uicolorpalette"></a>

The theme colors that apply to UI and to charts, excluding data colors\. The colors description is a hexadecimal color code that consists of six alphanumerical characters, prefixed with `#`, for example \#37BFF5\. For more information, see [Using Themes in Amazon QuickSight](https://docs.aws.amazon.com/quicksight/latest/user/themes-in-quicksight.html) in the *Amazon QuickSight User Guide\.* 

## Syntax<a name="aws-properties-quicksight-theme-uicolorpalette-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-theme-uicolorpalette-syntax.json"></a>

```
{
  "[Accent](#cfn-quicksight-theme-uicolorpalette-accent)" : String,
  "[AccentForeground](#cfn-quicksight-theme-uicolorpalette-accentforeground)" : String,
  "[Danger](#cfn-quicksight-theme-uicolorpalette-danger)" : String,
  "[DangerForeground](#cfn-quicksight-theme-uicolorpalette-dangerforeground)" : String,
  "[Dimension](#cfn-quicksight-theme-uicolorpalette-dimension)" : String,
  "[DimensionForeground](#cfn-quicksight-theme-uicolorpalette-dimensionforeground)" : String,
  "[Measure](#cfn-quicksight-theme-uicolorpalette-measure)" : String,
  "[MeasureForeground](#cfn-quicksight-theme-uicolorpalette-measureforeground)" : String,
  "[PrimaryBackground](#cfn-quicksight-theme-uicolorpalette-primarybackground)" : String,
  "[PrimaryForeground](#cfn-quicksight-theme-uicolorpalette-primaryforeground)" : String,
  "[SecondaryBackground](#cfn-quicksight-theme-uicolorpalette-secondarybackground)" : String,
  "[SecondaryForeground](#cfn-quicksight-theme-uicolorpalette-secondaryforeground)" : String,
  "[Success](#cfn-quicksight-theme-uicolorpalette-success)" : String,
  "[SuccessForeground](#cfn-quicksight-theme-uicolorpalette-successforeground)" : String,
  "[Warning](#cfn-quicksight-theme-uicolorpalette-warning)" : String,
  "[WarningForeground](#cfn-quicksight-theme-uicolorpalette-warningforeground)" : String
}
```

### YAML<a name="aws-properties-quicksight-theme-uicolorpalette-syntax.yaml"></a>

```
  [Accent](#cfn-quicksight-theme-uicolorpalette-accent): String
  [AccentForeground](#cfn-quicksight-theme-uicolorpalette-accentforeground): String
  [Danger](#cfn-quicksight-theme-uicolorpalette-danger): String
  [DangerForeground](#cfn-quicksight-theme-uicolorpalette-dangerforeground): String
  [Dimension](#cfn-quicksight-theme-uicolorpalette-dimension): String
  [DimensionForeground](#cfn-quicksight-theme-uicolorpalette-dimensionforeground): String
  [Measure](#cfn-quicksight-theme-uicolorpalette-measure): String
  [MeasureForeground](#cfn-quicksight-theme-uicolorpalette-measureforeground): String
  [PrimaryBackground](#cfn-quicksight-theme-uicolorpalette-primarybackground): String
  [PrimaryForeground](#cfn-quicksight-theme-uicolorpalette-primaryforeground): String
  [SecondaryBackground](#cfn-quicksight-theme-uicolorpalette-secondarybackground): String
  [SecondaryForeground](#cfn-quicksight-theme-uicolorpalette-secondaryforeground): String
  [Success](#cfn-quicksight-theme-uicolorpalette-success): String
  [SuccessForeground](#cfn-quicksight-theme-uicolorpalette-successforeground): String
  [Warning](#cfn-quicksight-theme-uicolorpalette-warning): String
  [WarningForeground](#cfn-quicksight-theme-uicolorpalette-warningforeground): String
```

## Properties<a name="aws-properties-quicksight-theme-uicolorpalette-properties"></a>

`Accent`  <a name="cfn-quicksight-theme-uicolorpalette-accent"></a>
This color is that applies to selected states and buttons\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AccentForeground`  <a name="cfn-quicksight-theme-uicolorpalette-accentforeground"></a>
The foreground color that applies to any text or other elements that appear over the accent color\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Danger`  <a name="cfn-quicksight-theme-uicolorpalette-danger"></a>
The color that applies to error messages\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DangerForeground`  <a name="cfn-quicksight-theme-uicolorpalette-dangerforeground"></a>
The foreground color that applies to any text or other elements that appear over the error color\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Dimension`  <a name="cfn-quicksight-theme-uicolorpalette-dimension"></a>
The color that applies to the names of fields that are identified as dimensions\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DimensionForeground`  <a name="cfn-quicksight-theme-uicolorpalette-dimensionforeground"></a>
The foreground color that applies to any text or other elements that appear over the dimension color\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Measure`  <a name="cfn-quicksight-theme-uicolorpalette-measure"></a>
The color that applies to the names of fields that are identified as measures\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MeasureForeground`  <a name="cfn-quicksight-theme-uicolorpalette-measureforeground"></a>
The foreground color that applies to any text or other elements that appear over the measure color\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryBackground`  <a name="cfn-quicksight-theme-uicolorpalette-primarybackground"></a>
The background color that applies to visuals and other high emphasis UI\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryForeground`  <a name="cfn-quicksight-theme-uicolorpalette-primaryforeground"></a>
The color of text and other foreground elements that appear over the primary background regions, such as grid lines, borders, table banding, icons, and so on\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondaryBackground`  <a name="cfn-quicksight-theme-uicolorpalette-secondarybackground"></a>
The background color that applies to the sheet background and sheet controls\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondaryForeground`  <a name="cfn-quicksight-theme-uicolorpalette-secondaryforeground"></a>
The foreground color that applies to any sheet title, sheet control text, or UI that appears over the secondary background\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Success`  <a name="cfn-quicksight-theme-uicolorpalette-success"></a>
The color that applies to success messages, for example the check mark for a successful download\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuccessForeground`  <a name="cfn-quicksight-theme-uicolorpalette-successforeground"></a>
The foreground color that applies to any text or other elements that appear over the success color\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Warning`  <a name="cfn-quicksight-theme-uicolorpalette-warning"></a>
This color that applies to warning and informational messages\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WarningForeground`  <a name="cfn-quicksight-theme-uicolorpalette-warningforeground"></a>
The foreground color that applies to any text or other elements that appear over the warning color\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)