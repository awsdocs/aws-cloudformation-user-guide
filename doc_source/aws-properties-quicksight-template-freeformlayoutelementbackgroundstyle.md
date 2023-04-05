# AWS::QuickSight::Template FreeFormLayoutElementBackgroundStyle<a name="aws-properties-quicksight-template-freeformlayoutelementbackgroundstyle"></a>

The background style configuration of a free\-form layout element\.

## Syntax<a name="aws-properties-quicksight-template-freeformlayoutelementbackgroundstyle-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-freeformlayoutelementbackgroundstyle-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-template-freeformlayoutelementbackgroundstyle-color)" : String,
  "[Visibility](#cfn-quicksight-template-freeformlayoutelementbackgroundstyle-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-freeformlayoutelementbackgroundstyle-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-template-freeformlayoutelementbackgroundstyle-color): String
  [Visibility](#cfn-quicksight-template-freeformlayoutelementbackgroundstyle-visibility): String
```

## Properties<a name="aws-properties-quicksight-template-freeformlayoutelementbackgroundstyle-properties"></a>

`Color`  <a name="cfn-quicksight-template-freeformlayoutelementbackgroundstyle-color"></a>
The background color of a free\-form layout element\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}(?:[A-F0-9]{2})?$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-template-freeformlayoutelementbackgroundstyle-visibility"></a>
The background visibility of a free\-form layout element\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)