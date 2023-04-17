# AWS::QuickSight::Template DefaultNewSheetConfiguration<a name="aws-properties-quicksight-template-defaultnewsheetconfiguration"></a>

The configuration for default new sheet settings\.

## Syntax<a name="aws-properties-quicksight-template-defaultnewsheetconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-defaultnewsheetconfiguration-syntax.json"></a>

```
{
  "[InteractiveLayoutConfiguration](#cfn-quicksight-template-defaultnewsheetconfiguration-interactivelayoutconfiguration)" : DefaultInteractiveLayoutConfiguration,
  "[PaginatedLayoutConfiguration](#cfn-quicksight-template-defaultnewsheetconfiguration-paginatedlayoutconfiguration)" : DefaultPaginatedLayoutConfiguration,
  "[SheetContentType](#cfn-quicksight-template-defaultnewsheetconfiguration-sheetcontenttype)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-defaultnewsheetconfiguration-syntax.yaml"></a>

```
  [InteractiveLayoutConfiguration](#cfn-quicksight-template-defaultnewsheetconfiguration-interactivelayoutconfiguration): 
    DefaultInteractiveLayoutConfiguration
  [PaginatedLayoutConfiguration](#cfn-quicksight-template-defaultnewsheetconfiguration-paginatedlayoutconfiguration): 
    DefaultPaginatedLayoutConfiguration
  [SheetContentType](#cfn-quicksight-template-defaultnewsheetconfiguration-sheetcontenttype): String
```

## Properties<a name="aws-properties-quicksight-template-defaultnewsheetconfiguration-properties"></a>

`InteractiveLayoutConfiguration`  <a name="cfn-quicksight-template-defaultnewsheetconfiguration-interactivelayoutconfiguration"></a>
The options that determine the default settings for interactive layout configuration\.  
*Required*: No  
*Type*: [DefaultInteractiveLayoutConfiguration](aws-properties-quicksight-template-defaultinteractivelayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PaginatedLayoutConfiguration`  <a name="cfn-quicksight-template-defaultnewsheetconfiguration-paginatedlayoutconfiguration"></a>
The options that determine the default settings for a paginated layout configuration\.  
*Required*: No  
*Type*: [DefaultPaginatedLayoutConfiguration](aws-properties-quicksight-template-defaultpaginatedlayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SheetContentType`  <a name="cfn-quicksight-template-defaultnewsheetconfiguration-sheetcontenttype"></a>
The option that determines the sheet content type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `INTERACTIVE | PAGINATED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)