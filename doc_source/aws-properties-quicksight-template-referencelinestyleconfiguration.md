# AWS::QuickSight::Template ReferenceLineStyleConfiguration<a name="aws-properties-quicksight-template-referencelinestyleconfiguration"></a>

The style configuration of the reference line\.

## Syntax<a name="aws-properties-quicksight-template-referencelinestyleconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-referencelinestyleconfiguration-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-template-referencelinestyleconfiguration-color)" : String,
  "[Pattern](#cfn-quicksight-template-referencelinestyleconfiguration-pattern)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-referencelinestyleconfiguration-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-template-referencelinestyleconfiguration-color): String
  [Pattern](#cfn-quicksight-template-referencelinestyleconfiguration-pattern): String
```

## Properties<a name="aws-properties-quicksight-template-referencelinestyleconfiguration-properties"></a>

`Color`  <a name="cfn-quicksight-template-referencelinestyleconfiguration-color"></a>
The hex color of the reference line\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Pattern`  <a name="cfn-quicksight-template-referencelinestyleconfiguration-pattern"></a>
The pattern type of the line style\. Choose one of the following options:  
+  `SOLID` 
+  `DASHED` 
+  `DOTTED` 
*Required*: No  
*Type*: String  
*Allowed values*: `DASHED | DOTTED | SOLID`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)