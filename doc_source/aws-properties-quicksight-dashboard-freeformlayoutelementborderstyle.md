# AWS::QuickSight::Dashboard FreeFormLayoutElementBorderStyle<a name="aws-properties-quicksight-dashboard-freeformlayoutelementborderstyle"></a>

The background style configuration of a free\-form layout element\.

## Syntax<a name="aws-properties-quicksight-dashboard-freeformlayoutelementborderstyle-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-freeformlayoutelementborderstyle-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-dashboard-freeformlayoutelementborderstyle-color)" : String,
  "[Visibility](#cfn-quicksight-dashboard-freeformlayoutelementborderstyle-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-freeformlayoutelementborderstyle-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-dashboard-freeformlayoutelementborderstyle-color): String
  [Visibility](#cfn-quicksight-dashboard-freeformlayoutelementborderstyle-visibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-freeformlayoutelementborderstyle-properties"></a>

`Color`  <a name="cfn-quicksight-dashboard-freeformlayoutelementborderstyle-color"></a>
The border color of a free\-form layout element\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}(?:[A-F0-9]{2})?$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-dashboard-freeformlayoutelementborderstyle-visibility"></a>
The border visibility of a free\-form layout element\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)