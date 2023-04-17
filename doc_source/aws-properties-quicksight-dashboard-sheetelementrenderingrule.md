# AWS::QuickSight::Dashboard SheetElementRenderingRule<a name="aws-properties-quicksight-dashboard-sheetelementrenderingrule"></a>

The rendering rules of a sheet that uses a free\-form layout\.

## Syntax<a name="aws-properties-quicksight-dashboard-sheetelementrenderingrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-sheetelementrenderingrule-syntax.json"></a>

```
{
  "[ConfigurationOverrides](#cfn-quicksight-dashboard-sheetelementrenderingrule-configurationoverrides)" : SheetElementConfigurationOverrides,
  "[Expression](#cfn-quicksight-dashboard-sheetelementrenderingrule-expression)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-sheetelementrenderingrule-syntax.yaml"></a>

```
  [ConfigurationOverrides](#cfn-quicksight-dashboard-sheetelementrenderingrule-configurationoverrides): 
    SheetElementConfigurationOverrides
  [Expression](#cfn-quicksight-dashboard-sheetelementrenderingrule-expression): String
```

## Properties<a name="aws-properties-quicksight-dashboard-sheetelementrenderingrule-properties"></a>

`ConfigurationOverrides`  <a name="cfn-quicksight-dashboard-sheetelementrenderingrule-configurationoverrides"></a>
The override configuration of the rendering rules of a sheet\.  
*Required*: Yes  
*Type*: [SheetElementConfigurationOverrides](aws-properties-quicksight-dashboard-sheetelementconfigurationoverrides.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-quicksight-dashboard-sheetelementrenderingrule-expression"></a>
The expression of the rendering rules of a sheet\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)