# AWS::QuickSight::Dashboard DataPointDrillUpDownOption<a name="aws-properties-quicksight-dashboard-datapointdrillupdownoption"></a>

The drill down options for data points in a dashbaord\.

## Syntax<a name="aws-properties-quicksight-dashboard-datapointdrillupdownoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-datapointdrillupdownoption-syntax.json"></a>

```
{
  "[AvailabilityStatus](#cfn-quicksight-dashboard-datapointdrillupdownoption-availabilitystatus)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-datapointdrillupdownoption-syntax.yaml"></a>

```
  [AvailabilityStatus](#cfn-quicksight-dashboard-datapointdrillupdownoption-availabilitystatus): String
```

## Properties<a name="aws-properties-quicksight-dashboard-datapointdrillupdownoption-properties"></a>

`AvailabilityStatus`  <a name="cfn-quicksight-dashboard-datapointdrillupdownoption-availabilitystatus"></a>
The status of the drill down options of data points\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)