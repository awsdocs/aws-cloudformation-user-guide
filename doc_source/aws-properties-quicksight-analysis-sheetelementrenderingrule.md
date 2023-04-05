# AWS::QuickSight::Analysis SheetElementRenderingRule<a name="aws-properties-quicksight-analysis-sheetelementrenderingrule"></a>

The rendering rules of a sheet that uses a free\-form layout\.

## Syntax<a name="aws-properties-quicksight-analysis-sheetelementrenderingrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-sheetelementrenderingrule-syntax.json"></a>

```
{
  "[ConfigurationOverrides](#cfn-quicksight-analysis-sheetelementrenderingrule-configurationoverrides)" : SheetElementConfigurationOverrides,
  "[Expression](#cfn-quicksight-analysis-sheetelementrenderingrule-expression)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-sheetelementrenderingrule-syntax.yaml"></a>

```
  [ConfigurationOverrides](#cfn-quicksight-analysis-sheetelementrenderingrule-configurationoverrides): 
    SheetElementConfigurationOverrides
  [Expression](#cfn-quicksight-analysis-sheetelementrenderingrule-expression): String
```

## Properties<a name="aws-properties-quicksight-analysis-sheetelementrenderingrule-properties"></a>

`ConfigurationOverrides`  <a name="cfn-quicksight-analysis-sheetelementrenderingrule-configurationoverrides"></a>
The override configuration of the rendering rules of a sheet\.  
*Required*: Yes  
*Type*: [SheetElementConfigurationOverrides](aws-properties-quicksight-analysis-sheetelementconfigurationoverrides.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-quicksight-analysis-sheetelementrenderingrule-expression"></a>
The expression of the rendering rules of a sheet\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)