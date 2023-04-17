# AWS::QuickSight::Dashboard DashboardVisualPublishOptions<a name="aws-properties-quicksight-dashboard-dashboardvisualpublishoptions"></a>

The visual publish options of a visual in a dashboard

## Syntax<a name="aws-properties-quicksight-dashboard-dashboardvisualpublishoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-dashboardvisualpublishoptions-syntax.json"></a>

```
{
  "[ExportHiddenFieldsOption](#cfn-quicksight-dashboard-dashboardvisualpublishoptions-exporthiddenfieldsoption)" : ExportHiddenFieldsOption
}
```

### YAML<a name="aws-properties-quicksight-dashboard-dashboardvisualpublishoptions-syntax.yaml"></a>

```
  [ExportHiddenFieldsOption](#cfn-quicksight-dashboard-dashboardvisualpublishoptions-exporthiddenfieldsoption): 
    ExportHiddenFieldsOption
```

## Properties<a name="aws-properties-quicksight-dashboard-dashboardvisualpublishoptions-properties"></a>

`ExportHiddenFieldsOption`  <a name="cfn-quicksight-dashboard-dashboardvisualpublishoptions-exporthiddenfieldsoption"></a>
Determines if hidden fields are included in an exported dashboard\.  
*Required*: No  
*Type*: [ExportHiddenFieldsOption](aws-properties-quicksight-dashboard-exporthiddenfieldsoption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)