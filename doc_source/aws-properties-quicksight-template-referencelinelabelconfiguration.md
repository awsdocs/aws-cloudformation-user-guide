# AWS::QuickSight::Template ReferenceLineLabelConfiguration<a name="aws-properties-quicksight-template-referencelinelabelconfiguration"></a>

The label configuration of a reference line\.

## Syntax<a name="aws-properties-quicksight-template-referencelinelabelconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-referencelinelabelconfiguration-syntax.json"></a>

```
{
  "[CustomLabelConfiguration](#cfn-quicksight-template-referencelinelabelconfiguration-customlabelconfiguration)" : ReferenceLineCustomLabelConfiguration,
  "[FontColor](#cfn-quicksight-template-referencelinelabelconfiguration-fontcolor)" : String,
  "[FontConfiguration](#cfn-quicksight-template-referencelinelabelconfiguration-fontconfiguration)" : FontConfiguration,
  "[HorizontalPosition](#cfn-quicksight-template-referencelinelabelconfiguration-horizontalposition)" : String,
  "[ValueLabelConfiguration](#cfn-quicksight-template-referencelinelabelconfiguration-valuelabelconfiguration)" : ReferenceLineValueLabelConfiguration,
  "[VerticalPosition](#cfn-quicksight-template-referencelinelabelconfiguration-verticalposition)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-referencelinelabelconfiguration-syntax.yaml"></a>

```
  [CustomLabelConfiguration](#cfn-quicksight-template-referencelinelabelconfiguration-customlabelconfiguration): 
    ReferenceLineCustomLabelConfiguration
  [FontColor](#cfn-quicksight-template-referencelinelabelconfiguration-fontcolor): String
  [FontConfiguration](#cfn-quicksight-template-referencelinelabelconfiguration-fontconfiguration): 
    FontConfiguration
  [HorizontalPosition](#cfn-quicksight-template-referencelinelabelconfiguration-horizontalposition): String
  [ValueLabelConfiguration](#cfn-quicksight-template-referencelinelabelconfiguration-valuelabelconfiguration): 
    ReferenceLineValueLabelConfiguration
  [VerticalPosition](#cfn-quicksight-template-referencelinelabelconfiguration-verticalposition): String
```

## Properties<a name="aws-properties-quicksight-template-referencelinelabelconfiguration-properties"></a>

`CustomLabelConfiguration`  <a name="cfn-quicksight-template-referencelinelabelconfiguration-customlabelconfiguration"></a>
The custom label configuration of the label in a reference line\.  
*Required*: No  
*Type*: [ReferenceLineCustomLabelConfiguration](aws-properties-quicksight-template-referencelinecustomlabelconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontColor`  <a name="cfn-quicksight-template-referencelinelabelconfiguration-fontcolor"></a>
The font color configuration of the label in a reference line\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontConfiguration`  <a name="cfn-quicksight-template-referencelinelabelconfiguration-fontconfiguration"></a>
The font configuration of the label in a reference line\.  
*Required*: No  
*Type*: [FontConfiguration](aws-properties-quicksight-template-fontconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HorizontalPosition`  <a name="cfn-quicksight-template-referencelinelabelconfiguration-horizontalposition"></a>
The horizontal position configuration of the label in a reference line\. Choose one of the following options:  
+  `LEFT` 
+  `CENTER` 
+  `RIGHT` 
*Required*: No  
*Type*: String  
*Allowed values*: `CENTER | LEFT | RIGHT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueLabelConfiguration`  <a name="cfn-quicksight-template-referencelinelabelconfiguration-valuelabelconfiguration"></a>
The value label configuration of the label in a reference line\.  
*Required*: No  
*Type*: [ReferenceLineValueLabelConfiguration](aws-properties-quicksight-template-referencelinevaluelabelconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerticalPosition`  <a name="cfn-quicksight-template-referencelinelabelconfiguration-verticalposition"></a>
The vertical position configuration of the label in a reference line\. Choose one of the following options:  
+  `ABOVE` 
+  `BELOW` 
*Required*: No  
*Type*: String  
*Allowed values*: `ABOVE | BELOW`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)