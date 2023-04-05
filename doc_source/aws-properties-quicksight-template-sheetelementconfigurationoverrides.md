# AWS::QuickSight::Template SheetElementConfigurationOverrides<a name="aws-properties-quicksight-template-sheetelementconfigurationoverrides"></a>

The override configuration of the rendering rules of a sheet\.

## Syntax<a name="aws-properties-quicksight-template-sheetelementconfigurationoverrides-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-sheetelementconfigurationoverrides-syntax.json"></a>

```
{
  "[Visibility](#cfn-quicksight-template-sheetelementconfigurationoverrides-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-sheetelementconfigurationoverrides-syntax.yaml"></a>

```
  [Visibility](#cfn-quicksight-template-sheetelementconfigurationoverrides-visibility): String
```

## Properties<a name="aws-properties-quicksight-template-sheetelementconfigurationoverrides-properties"></a>

`Visibility`  <a name="cfn-quicksight-template-sheetelementconfigurationoverrides-visibility"></a>
Determines whether or not the overrides are visible\. Choose one of the following options:  
+  `VISIBLE` 
+  `HIDDEN` 
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)