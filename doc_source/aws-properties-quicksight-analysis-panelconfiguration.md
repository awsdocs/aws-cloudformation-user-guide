# AWS::QuickSight::Analysis PanelConfiguration<a name="aws-properties-quicksight-analysis-panelconfiguration"></a>

A collection of options that configure how each panel displays in a small multiples chart\.

## Syntax<a name="aws-properties-quicksight-analysis-panelconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-panelconfiguration-syntax.json"></a>

```
{
  "[BackgroundColor](#cfn-quicksight-analysis-panelconfiguration-backgroundcolor)" : String,
  "[BackgroundVisibility](#cfn-quicksight-analysis-panelconfiguration-backgroundvisibility)" : String,
  "[BorderColor](#cfn-quicksight-analysis-panelconfiguration-bordercolor)" : String,
  "[BorderStyle](#cfn-quicksight-analysis-panelconfiguration-borderstyle)" : String,
  "[BorderThickness](#cfn-quicksight-analysis-panelconfiguration-borderthickness)" : String,
  "[BorderVisibility](#cfn-quicksight-analysis-panelconfiguration-bordervisibility)" : String,
  "[GutterSpacing](#cfn-quicksight-analysis-panelconfiguration-gutterspacing)" : String,
  "[GutterVisibility](#cfn-quicksight-analysis-panelconfiguration-guttervisibility)" : String,
  "[Title](#cfn-quicksight-analysis-panelconfiguration-title)" : PanelTitleOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-panelconfiguration-syntax.yaml"></a>

```
  [BackgroundColor](#cfn-quicksight-analysis-panelconfiguration-backgroundcolor): String
  [BackgroundVisibility](#cfn-quicksight-analysis-panelconfiguration-backgroundvisibility): String
  [BorderColor](#cfn-quicksight-analysis-panelconfiguration-bordercolor): String
  [BorderStyle](#cfn-quicksight-analysis-panelconfiguration-borderstyle): String
  [BorderThickness](#cfn-quicksight-analysis-panelconfiguration-borderthickness): String
  [BorderVisibility](#cfn-quicksight-analysis-panelconfiguration-bordervisibility): String
  [GutterSpacing](#cfn-quicksight-analysis-panelconfiguration-gutterspacing): String
  [GutterVisibility](#cfn-quicksight-analysis-panelconfiguration-guttervisibility): String
  [Title](#cfn-quicksight-analysis-panelconfiguration-title): 
    PanelTitleOptions
```

## Properties<a name="aws-properties-quicksight-analysis-panelconfiguration-properties"></a>

`BackgroundColor`  <a name="cfn-quicksight-analysis-panelconfiguration-backgroundcolor"></a>
Sets the background color for each panel\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}(?:[A-F0-9]{2})?$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BackgroundVisibility`  <a name="cfn-quicksight-analysis-panelconfiguration-backgroundvisibility"></a>
Determines whether or not a background for each small multiples panel is rendered\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BorderColor`  <a name="cfn-quicksight-analysis-panelconfiguration-bordercolor"></a>
Sets the line color of panel borders\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}(?:[A-F0-9]{2})?$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BorderStyle`  <a name="cfn-quicksight-analysis-panelconfiguration-borderstyle"></a>
Sets the line style of panel borders\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DASHED | DOTTED | SOLID`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BorderThickness`  <a name="cfn-quicksight-analysis-panelconfiguration-borderthickness"></a>
Sets the line thickness of panel borders\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BorderVisibility`  <a name="cfn-quicksight-analysis-panelconfiguration-bordervisibility"></a>
Determines whether or not each panel displays a border\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GutterSpacing`  <a name="cfn-quicksight-analysis-panelconfiguration-gutterspacing"></a>
Sets the total amount of negative space to display between sibling panels\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GutterVisibility`  <a name="cfn-quicksight-analysis-panelconfiguration-guttervisibility"></a>
Determines whether or not negative space between sibling panels is rendered\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-analysis-panelconfiguration-title"></a>
Configures the title display within each small multiples panel\.  
*Required*: No  
*Type*: [PanelTitleOptions](aws-properties-quicksight-analysis-paneltitleoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)