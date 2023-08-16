# AWS::QuickSight::Template FilterScopeConfiguration<a name="aws-properties-quicksight-template-filterscopeconfiguration"></a>

The scope configuration for a `FilterGroup`\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-filterscopeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-filterscopeconfiguration-syntax.json"></a>

```
{
  "[SelectedSheets](#cfn-quicksight-template-filterscopeconfiguration-selectedsheets)" : SelectedSheetsFilterScopeConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-filterscopeconfiguration-syntax.yaml"></a>

```
  [SelectedSheets](#cfn-quicksight-template-filterscopeconfiguration-selectedsheets): 
    SelectedSheetsFilterScopeConfiguration
```

## Properties<a name="aws-properties-quicksight-template-filterscopeconfiguration-properties"></a>

`SelectedSheets`  <a name="cfn-quicksight-template-filterscopeconfiguration-selectedsheets"></a>
The configuration for applying a filter to specific sheets\.  
*Required*: No  
*Type*: [SelectedSheetsFilterScopeConfiguration](aws-properties-quicksight-template-selectedsheetsfilterscopeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)