# AWS::QuickSight::Dashboard SheetVisualScopingConfiguration<a name="aws-properties-quicksight-dashboard-sheetvisualscopingconfiguration"></a>

The filter that is applied to the options\.

## Syntax<a name="aws-properties-quicksight-dashboard-sheetvisualscopingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-sheetvisualscopingconfiguration-syntax.json"></a>

```
{
  "[Scope](#cfn-quicksight-dashboard-sheetvisualscopingconfiguration-scope)" : String,
  "[SheetId](#cfn-quicksight-dashboard-sheetvisualscopingconfiguration-sheetid)" : String,
  "[VisualIds](#cfn-quicksight-dashboard-sheetvisualscopingconfiguration-visualids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-sheetvisualscopingconfiguration-syntax.yaml"></a>

```
  [Scope](#cfn-quicksight-dashboard-sheetvisualscopingconfiguration-scope): String
  [SheetId](#cfn-quicksight-dashboard-sheetvisualscopingconfiguration-sheetid): String
  [VisualIds](#cfn-quicksight-dashboard-sheetvisualscopingconfiguration-visualids): 
    - String
```

## Properties<a name="aws-properties-quicksight-dashboard-sheetvisualscopingconfiguration-properties"></a>

`Scope`  <a name="cfn-quicksight-dashboard-sheetvisualscopingconfiguration-scope"></a>
The scope of the applied entities\. Choose one of the following options:  
+  `ALL_VISUALS` 
+  `SELECTED_VISUALS` 
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALL_VISUALS | SELECTED_VISUALS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SheetId`  <a name="cfn-quicksight-dashboard-sheetvisualscopingconfiguration-sheetid"></a>
The selected sheet that the filter is applied to\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualIds`  <a name="cfn-quicksight-dashboard-sheetvisualscopingconfiguration-visualids"></a>
The selected visuals that the filter is applied to\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)