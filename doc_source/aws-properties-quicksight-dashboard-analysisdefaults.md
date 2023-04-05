# AWS::QuickSight::Dashboard AnalysisDefaults<a name="aws-properties-quicksight-dashboard-analysisdefaults"></a>

The configuration for default analysis settings\.

## Syntax<a name="aws-properties-quicksight-dashboard-analysisdefaults-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-analysisdefaults-syntax.json"></a>

```
{
  "[DefaultNewSheetConfiguration](#cfn-quicksight-dashboard-analysisdefaults-defaultnewsheetconfiguration)" : DefaultNewSheetConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-analysisdefaults-syntax.yaml"></a>

```
  [DefaultNewSheetConfiguration](#cfn-quicksight-dashboard-analysisdefaults-defaultnewsheetconfiguration): 
    DefaultNewSheetConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-analysisdefaults-properties"></a>

`DefaultNewSheetConfiguration`  <a name="cfn-quicksight-dashboard-analysisdefaults-defaultnewsheetconfiguration"></a>
The configuration for default new sheet settings\.  
*Required*: Yes  
*Type*: [DefaultNewSheetConfiguration](aws-properties-quicksight-dashboard-defaultnewsheetconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)