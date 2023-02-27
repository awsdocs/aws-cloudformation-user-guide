# AWS::QuickSight::Dashboard DashboardError<a name="aws-properties-quicksight-dashboard-dashboarderror"></a>

Dashboard error\.

## Syntax<a name="aws-properties-quicksight-dashboard-dashboarderror-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-dashboarderror-syntax.json"></a>

```
{
  "[Message](#cfn-quicksight-dashboard-dashboarderror-message)" : String,
  "[Type](#cfn-quicksight-dashboard-dashboarderror-type)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-dashboarderror-syntax.yaml"></a>

```
  [Message](#cfn-quicksight-dashboard-dashboarderror-message): String
  [Type](#cfn-quicksight-dashboard-dashboarderror-type): String
```

## Properties<a name="aws-properties-quicksight-dashboard-dashboarderror-properties"></a>

`Message`  <a name="cfn-quicksight-dashboard-dashboarderror-message"></a>
Message\.  
*Required*: No  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-dashboard-dashboarderror-type"></a>
Type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ACCESS_DENIED | COLUMN_GEOGRAPHIC_ROLE_MISMATCH | COLUMN_REPLACEMENT_MISSING | COLUMN_TYPE_MISMATCH | DATA_SET_NOT_FOUND | INTERNAL_FAILURE | PARAMETER_NOT_FOUND | PARAMETER_TYPE_INVALID | PARAMETER_VALUE_INCOMPATIBLE | SOURCE_NOT_FOUND`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)