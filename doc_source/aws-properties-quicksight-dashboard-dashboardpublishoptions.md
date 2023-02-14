# AWS::QuickSight::Dashboard DashboardPublishOptions<a name="aws-properties-quicksight-dashboard-dashboardpublishoptions"></a>

Dashboard publish options\.

## Syntax<a name="aws-properties-quicksight-dashboard-dashboardpublishoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-dashboardpublishoptions-syntax.json"></a>

```
{
  "[AdHocFilteringOption](#cfn-quicksight-dashboard-dashboardpublishoptions-adhocfilteringoption)" : AdHocFilteringOption,
  "[ExportToCSVOption](#cfn-quicksight-dashboard-dashboardpublishoptions-exporttocsvoption)" : ExportToCSVOption,
  "[SheetControlsOption](#cfn-quicksight-dashboard-dashboardpublishoptions-sheetcontrolsoption)" : SheetControlsOption
}
```

### YAML<a name="aws-properties-quicksight-dashboard-dashboardpublishoptions-syntax.yaml"></a>

```
  [AdHocFilteringOption](#cfn-quicksight-dashboard-dashboardpublishoptions-adhocfilteringoption): 
    AdHocFilteringOption
  [ExportToCSVOption](#cfn-quicksight-dashboard-dashboardpublishoptions-exporttocsvoption): 
    ExportToCSVOption
  [SheetControlsOption](#cfn-quicksight-dashboard-dashboardpublishoptions-sheetcontrolsoption): 
    SheetControlsOption
```

## Properties<a name="aws-properties-quicksight-dashboard-dashboardpublishoptions-properties"></a>

`AdHocFilteringOption`  <a name="cfn-quicksight-dashboard-dashboardpublishoptions-adhocfilteringoption"></a>
Ad hoc \(one\-time\) filtering option\.  
*Required*: No  
*Type*: [AdHocFilteringOption](aws-properties-quicksight-dashboard-adhocfilteringoption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExportToCSVOption`  <a name="cfn-quicksight-dashboard-dashboardpublishoptions-exporttocsvoption"></a>
Export to \.csv option\.  
*Required*: No  
*Type*: [ExportToCSVOption](aws-properties-quicksight-dashboard-exporttocsvoption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SheetControlsOption`  <a name="cfn-quicksight-dashboard-dashboardpublishoptions-sheetcontrolsoption"></a>
Sheet controls option\.  
*Required*: No  
*Type*: [SheetControlsOption](aws-properties-quicksight-dashboard-sheetcontrolsoption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)