# AWS::QuickSight::Analysis DefaultNewSheetConfiguration<a name="aws-properties-quicksight-analysis-defaultnewsheetconfiguration"></a>

The configuration for default new sheet settings\.

## Syntax<a name="aws-properties-quicksight-analysis-defaultnewsheetconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-defaultnewsheetconfiguration-syntax.json"></a>

```
{
  "[InteractiveLayoutConfiguration](#cfn-quicksight-analysis-defaultnewsheetconfiguration-interactivelayoutconfiguration)" : DefaultInteractiveLayoutConfiguration,
  "[PaginatedLayoutConfiguration](#cfn-quicksight-analysis-defaultnewsheetconfiguration-paginatedlayoutconfiguration)" : DefaultPaginatedLayoutConfiguration,
  "[SheetContentType](#cfn-quicksight-analysis-defaultnewsheetconfiguration-sheetcontenttype)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-defaultnewsheetconfiguration-syntax.yaml"></a>

```
  [InteractiveLayoutConfiguration](#cfn-quicksight-analysis-defaultnewsheetconfiguration-interactivelayoutconfiguration): 
    DefaultInteractiveLayoutConfiguration
  [PaginatedLayoutConfiguration](#cfn-quicksight-analysis-defaultnewsheetconfiguration-paginatedlayoutconfiguration): 
    DefaultPaginatedLayoutConfiguration
  [SheetContentType](#cfn-quicksight-analysis-defaultnewsheetconfiguration-sheetcontenttype): String
```

## Properties<a name="aws-properties-quicksight-analysis-defaultnewsheetconfiguration-properties"></a>

`InteractiveLayoutConfiguration`  <a name="cfn-quicksight-analysis-defaultnewsheetconfiguration-interactivelayoutconfiguration"></a>
The options that determine the default settings for interactive layout configuration\.  
*Required*: No  
*Type*: [DefaultInteractiveLayoutConfiguration](aws-properties-quicksight-analysis-defaultinteractivelayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PaginatedLayoutConfiguration`  <a name="cfn-quicksight-analysis-defaultnewsheetconfiguration-paginatedlayoutconfiguration"></a>
The options that determine the default settings for a paginated layout configuration\.  
*Required*: No  
*Type*: [DefaultPaginatedLayoutConfiguration](aws-properties-quicksight-analysis-defaultpaginatedlayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SheetContentType`  <a name="cfn-quicksight-analysis-defaultnewsheetconfiguration-sheetcontenttype"></a>
The option that determines the sheet content type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `INTERACTIVE | PAGINATED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)