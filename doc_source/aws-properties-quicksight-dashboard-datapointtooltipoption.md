# AWS::QuickSight::Dashboard DataPointTooltipOption<a name="aws-properties-quicksight-dashboard-datapointtooltipoption"></a>

The data point tooltip options\.

## Syntax<a name="aws-properties-quicksight-dashboard-datapointtooltipoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-datapointtooltipoption-syntax.json"></a>

```
{
  "[AvailabilityStatus](#cfn-quicksight-dashboard-datapointtooltipoption-availabilitystatus)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-datapointtooltipoption-syntax.yaml"></a>

```
  [AvailabilityStatus](#cfn-quicksight-dashboard-datapointtooltipoption-availabilitystatus): String
```

## Properties<a name="aws-properties-quicksight-dashboard-datapointtooltipoption-properties"></a>

`AvailabilityStatus`  <a name="cfn-quicksight-dashboard-datapointtooltipoption-availabilitystatus"></a>
The status of the data point tool tip options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)