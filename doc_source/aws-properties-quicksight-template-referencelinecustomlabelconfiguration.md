# AWS::QuickSight::Template ReferenceLineCustomLabelConfiguration<a name="aws-properties-quicksight-template-referencelinecustomlabelconfiguration"></a>

The configuration for a custom label on a `ReferenceLine`\.

## Syntax<a name="aws-properties-quicksight-template-referencelinecustomlabelconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-referencelinecustomlabelconfiguration-syntax.json"></a>

```
{
  "[CustomLabel](#cfn-quicksight-template-referencelinecustomlabelconfiguration-customlabel)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-referencelinecustomlabelconfiguration-syntax.yaml"></a>

```
  [CustomLabel](#cfn-quicksight-template-referencelinecustomlabelconfiguration-customlabel): String
```

## Properties<a name="aws-properties-quicksight-template-referencelinecustomlabelconfiguration-properties"></a>

`CustomLabel`  <a name="cfn-quicksight-template-referencelinecustomlabelconfiguration-customlabel"></a>
The string text of the custom label\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)