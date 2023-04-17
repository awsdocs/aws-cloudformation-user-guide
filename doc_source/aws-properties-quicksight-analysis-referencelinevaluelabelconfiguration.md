# AWS::QuickSight::Analysis ReferenceLineValueLabelConfiguration<a name="aws-properties-quicksight-analysis-referencelinevaluelabelconfiguration"></a>

The value label configuration of the label in a reference line\.

## Syntax<a name="aws-properties-quicksight-analysis-referencelinevaluelabelconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-referencelinevaluelabelconfiguration-syntax.json"></a>

```
{
  "[FormatConfiguration](#cfn-quicksight-analysis-referencelinevaluelabelconfiguration-formatconfiguration)" : NumericFormatConfiguration,
  "[RelativePosition](#cfn-quicksight-analysis-referencelinevaluelabelconfiguration-relativeposition)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-referencelinevaluelabelconfiguration-syntax.yaml"></a>

```
  [FormatConfiguration](#cfn-quicksight-analysis-referencelinevaluelabelconfiguration-formatconfiguration): 
    NumericFormatConfiguration
  [RelativePosition](#cfn-quicksight-analysis-referencelinevaluelabelconfiguration-relativeposition): String
```

## Properties<a name="aws-properties-quicksight-analysis-referencelinevaluelabelconfiguration-properties"></a>

`FormatConfiguration`  <a name="cfn-quicksight-analysis-referencelinevaluelabelconfiguration-formatconfiguration"></a>
The format configuration of the value label\.  
*Required*: No  
*Type*: [NumericFormatConfiguration](aws-properties-quicksight-analysis-numericformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelativePosition`  <a name="cfn-quicksight-analysis-referencelinevaluelabelconfiguration-relativeposition"></a>
The relative position of the value label\. Choose one of the following options:  
+  `BEFORE_CUSTOM_LABEL` 
+  `AFTER_CUSTOM_LABEL` 
*Required*: No  
*Type*: String  
*Allowed values*: `AFTER_CUSTOM_LABEL | BEFORE_CUSTOM_LABEL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)