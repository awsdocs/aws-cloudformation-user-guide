# AWS::QuickSight::Dashboard DataPointMenuLabelOption<a name="aws-properties-quicksight-dashboard-datapointmenulabeloption"></a>

The data point menu options of a dashboard\.

## Syntax<a name="aws-properties-quicksight-dashboard-datapointmenulabeloption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-datapointmenulabeloption-syntax.json"></a>

```
{
  "[AvailabilityStatus](#cfn-quicksight-dashboard-datapointmenulabeloption-availabilitystatus)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-datapointmenulabeloption-syntax.yaml"></a>

```
  [AvailabilityStatus](#cfn-quicksight-dashboard-datapointmenulabeloption-availabilitystatus): String
```

## Properties<a name="aws-properties-quicksight-dashboard-datapointmenulabeloption-properties"></a>

`AvailabilityStatus`  <a name="cfn-quicksight-dashboard-datapointmenulabeloption-availabilitystatus"></a>
The status of the data point menu options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)