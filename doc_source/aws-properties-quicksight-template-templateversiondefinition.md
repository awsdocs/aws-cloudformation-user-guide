# AWS::QuickSight::Template TemplateVersionDefinition<a name="aws-properties-quicksight-template-templateversiondefinition"></a>

The detailed definition of a template\.

## Syntax<a name="aws-properties-quicksight-template-templateversiondefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-templateversiondefinition-syntax.json"></a>

```
{
  "[AnalysisDefaults](#cfn-quicksight-template-templateversiondefinition-analysisdefaults)" : AnalysisDefaults,
  "[CalculatedFields](#cfn-quicksight-template-templateversiondefinition-calculatedfields)" : [ CalculatedField, ... ],
  "[ColumnConfigurations](#cfn-quicksight-template-templateversiondefinition-columnconfigurations)" : [ ColumnConfiguration, ... ],
  "[DataSetConfigurations](#cfn-quicksight-template-templateversiondefinition-datasetconfigurations)" : [ DataSetConfiguration, ... ],
  "[FilterGroups](#cfn-quicksight-template-templateversiondefinition-filtergroups)" : [ FilterGroup, ... ],
  "[ParameterDeclarations](#cfn-quicksight-template-templateversiondefinition-parameterdeclarations)" : [ ParameterDeclaration, ... ],
  "[Sheets](#cfn-quicksight-template-templateversiondefinition-sheets)" : [ SheetDefinition, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-templateversiondefinition-syntax.yaml"></a>

```
  [AnalysisDefaults](#cfn-quicksight-template-templateversiondefinition-analysisdefaults): 
    AnalysisDefaults
  [CalculatedFields](#cfn-quicksight-template-templateversiondefinition-calculatedfields): 
    - CalculatedField
  [ColumnConfigurations](#cfn-quicksight-template-templateversiondefinition-columnconfigurations): 
    - ColumnConfiguration
  [DataSetConfigurations](#cfn-quicksight-template-templateversiondefinition-datasetconfigurations): 
    - DataSetConfiguration
  [FilterGroups](#cfn-quicksight-template-templateversiondefinition-filtergroups): 
    - FilterGroup
  [ParameterDeclarations](#cfn-quicksight-template-templateversiondefinition-parameterdeclarations): 
    - ParameterDeclaration
  [Sheets](#cfn-quicksight-template-templateversiondefinition-sheets): 
    - SheetDefinition
```

## Properties<a name="aws-properties-quicksight-template-templateversiondefinition-properties"></a>

`AnalysisDefaults`  <a name="cfn-quicksight-template-templateversiondefinition-analysisdefaults"></a>
Property description not available\.  
*Required*: No  
*Type*: [AnalysisDefaults](aws-properties-quicksight-template-analysisdefaults.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CalculatedFields`  <a name="cfn-quicksight-template-templateversiondefinition-calculatedfields"></a>
An array of calculated field definitions for the template\.  
*Required*: No  
*Type*: List of [CalculatedField](aws-properties-quicksight-template-calculatedfield.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnConfigurations`  <a name="cfn-quicksight-template-templateversiondefinition-columnconfigurations"></a>
 An array of template\-level column configurations\. Column configurations are used to set default formatting for a column that's used throughout a template\.   
*Required*: No  
*Type*: List of [ColumnConfiguration](aws-properties-quicksight-template-columnconfiguration.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSetConfigurations`  <a name="cfn-quicksight-template-templateversiondefinition-datasetconfigurations"></a>
An array of dataset configurations\. These configurations define the required columns for each dataset used within a template\.  
*Required*: Yes  
*Type*: List of [DataSetConfiguration](aws-properties-quicksight-template-datasetconfiguration.md)  
*Maximum*: `30`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterGroups`  <a name="cfn-quicksight-template-templateversiondefinition-filtergroups"></a>
Filter definitions for a template\.  
For more information, see [Filtering Data](https://docs.aws.amazon.com/quicksight/latest/user/filtering-visual-data.html) in the *Amazon QuickSight User Guide*\.   
*Required*: No  
*Type*: List of [FilterGroup](aws-properties-quicksight-template-filtergroup.md)  
*Maximum*: `2000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterDeclarations`  <a name="cfn-quicksight-template-templateversiondefinition-parameterdeclarations"></a>
An array of parameter declarations for a template\.  
 *Parameters* are named variables that can transfer a value for use by an action or an object\.  
For more information, see [Parameters in Amazon QuickSight](https://docs.aws.amazon.com/quicksight/latest/user/parameters-in-quicksight.html) in the *Amazon QuickSight User Guide*\.   
*Required*: No  
*Type*: List of [ParameterDeclaration](aws-properties-quicksight-template-parameterdeclaration.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sheets`  <a name="cfn-quicksight-template-templateversiondefinition-sheets"></a>
An array of sheet definitions for a template\.  
*Required*: No  
*Type*: List of [SheetDefinition](aws-properties-quicksight-template-sheetdefinition.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)