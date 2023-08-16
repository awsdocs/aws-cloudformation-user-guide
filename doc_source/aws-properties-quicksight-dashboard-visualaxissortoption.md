# AWS::QuickSight::Dashboard VisualAxisSortOption<a name="aws-properties-quicksight-dashboard-visualaxissortoption"></a>

The axis sort options for a visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-visualaxissortoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-visualaxissortoption-syntax.json"></a>

```
{
  "[AvailabilityStatus](#cfn-quicksight-dashboard-visualaxissortoption-availabilitystatus)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-visualaxissortoption-syntax.yaml"></a>

```
  [AvailabilityStatus](#cfn-quicksight-dashboard-visualaxissortoption-availabilitystatus): String
```

## Properties<a name="aws-properties-quicksight-dashboard-visualaxissortoption-properties"></a>

`AvailabilityStatus`  <a name="cfn-quicksight-dashboard-visualaxissortoption-availabilitystatus"></a>
The availaiblity status of a visual's axis sort options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)