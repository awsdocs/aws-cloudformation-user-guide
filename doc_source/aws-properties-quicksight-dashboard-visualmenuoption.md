# AWS::QuickSight::Dashboard VisualMenuOption<a name="aws-properties-quicksight-dashboard-visualmenuoption"></a>

The menu options for a visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-visualmenuoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-visualmenuoption-syntax.json"></a>

```
{
  "[AvailabilityStatus](#cfn-quicksight-dashboard-visualmenuoption-availabilitystatus)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-visualmenuoption-syntax.yaml"></a>

```
  [AvailabilityStatus](#cfn-quicksight-dashboard-visualmenuoption-availabilitystatus): String
```

## Properties<a name="aws-properties-quicksight-dashboard-visualmenuoption-properties"></a>

`AvailabilityStatus`  <a name="cfn-quicksight-dashboard-visualmenuoption-availabilitystatus"></a>
The availaiblity status of a visual's menu options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)