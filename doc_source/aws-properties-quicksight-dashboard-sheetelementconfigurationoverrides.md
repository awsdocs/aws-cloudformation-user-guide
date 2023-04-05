# AWS::QuickSight::Dashboard SheetElementConfigurationOverrides<a name="aws-properties-quicksight-dashboard-sheetelementconfigurationoverrides"></a>

The override configuration of the rendering rules of a sheet\.

## Syntax<a name="aws-properties-quicksight-dashboard-sheetelementconfigurationoverrides-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-sheetelementconfigurationoverrides-syntax.json"></a>

```
{
  "[Visibility](#cfn-quicksight-dashboard-sheetelementconfigurationoverrides-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-sheetelementconfigurationoverrides-syntax.yaml"></a>

```
  [Visibility](#cfn-quicksight-dashboard-sheetelementconfigurationoverrides-visibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-sheetelementconfigurationoverrides-properties"></a>

`Visibility`  <a name="cfn-quicksight-dashboard-sheetelementconfigurationoverrides-visibility"></a>
Determines whether or not the overrides are visible\. Choose one of the following options:  
+  `VISIBLE` 
+  `HIDDEN` 
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)