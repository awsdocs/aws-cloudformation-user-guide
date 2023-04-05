# AWS::QuickSight::Dashboard ExportHiddenFieldsOption<a name="aws-properties-quicksight-dashboard-exporthiddenfieldsoption"></a>

Determines if hidden fields are included in an exported dashboard\.

## Syntax<a name="aws-properties-quicksight-dashboard-exporthiddenfieldsoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-exporthiddenfieldsoption-syntax.json"></a>

```
{
  "[AvailabilityStatus](#cfn-quicksight-dashboard-exporthiddenfieldsoption-availabilitystatus)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-exporthiddenfieldsoption-syntax.yaml"></a>

```
  [AvailabilityStatus](#cfn-quicksight-dashboard-exporthiddenfieldsoption-availabilitystatus): String
```

## Properties<a name="aws-properties-quicksight-dashboard-exporthiddenfieldsoption-properties"></a>

`AvailabilityStatus`  <a name="cfn-quicksight-dashboard-exporthiddenfieldsoption-availabilitystatus"></a>
The status of the export hidden fields options of a dashbaord\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)