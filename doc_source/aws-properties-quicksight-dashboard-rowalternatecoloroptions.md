# AWS::QuickSight::Dashboard RowAlternateColorOptions<a name="aws-properties-quicksight-dashboard-rowalternatecoloroptions"></a>

Determines the row alternate color options\.

## Syntax<a name="aws-properties-quicksight-dashboard-rowalternatecoloroptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-rowalternatecoloroptions-syntax.json"></a>

```
{
  "[RowAlternateColors](#cfn-quicksight-dashboard-rowalternatecoloroptions-rowalternatecolors)" : [ String, ... ],
  "[Status](#cfn-quicksight-dashboard-rowalternatecoloroptions-status)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-rowalternatecoloroptions-syntax.yaml"></a>

```
  [RowAlternateColors](#cfn-quicksight-dashboard-rowalternatecoloroptions-rowalternatecolors): 
    - String
  [Status](#cfn-quicksight-dashboard-rowalternatecoloroptions-status): String
```

## Properties<a name="aws-properties-quicksight-dashboard-rowalternatecoloroptions-properties"></a>

`RowAlternateColors`  <a name="cfn-quicksight-dashboard-rowalternatecoloroptions-rowalternatecolors"></a>
Determines the list of row alternate colors\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-quicksight-dashboard-rowalternatecoloroptions-status"></a>
Determines the widget status\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)