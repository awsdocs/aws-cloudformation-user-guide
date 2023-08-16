# AWS::QuickSight::Dashboard ComparisonFormatConfiguration<a name="aws-properties-quicksight-dashboard-comparisonformatconfiguration"></a>

The format of the comparison\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-comparisonformatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-comparisonformatconfiguration-syntax.json"></a>

```
{
  "[NumberDisplayFormatConfiguration](#cfn-quicksight-dashboard-comparisonformatconfiguration-numberdisplayformatconfiguration)" : NumberDisplayFormatConfiguration,
  "[PercentageDisplayFormatConfiguration](#cfn-quicksight-dashboard-comparisonformatconfiguration-percentagedisplayformatconfiguration)" : PercentageDisplayFormatConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-comparisonformatconfiguration-syntax.yaml"></a>

```
  [NumberDisplayFormatConfiguration](#cfn-quicksight-dashboard-comparisonformatconfiguration-numberdisplayformatconfiguration): 
    NumberDisplayFormatConfiguration
  [PercentageDisplayFormatConfiguration](#cfn-quicksight-dashboard-comparisonformatconfiguration-percentagedisplayformatconfiguration): 
    PercentageDisplayFormatConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-comparisonformatconfiguration-properties"></a>

`NumberDisplayFormatConfiguration`  <a name="cfn-quicksight-dashboard-comparisonformatconfiguration-numberdisplayformatconfiguration"></a>
The number display format\.  
*Required*: No  
*Type*: [NumberDisplayFormatConfiguration](aws-properties-quicksight-dashboard-numberdisplayformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PercentageDisplayFormatConfiguration`  <a name="cfn-quicksight-dashboard-comparisonformatconfiguration-percentagedisplayformatconfiguration"></a>
The percentage display format\.  
*Required*: No  
*Type*: [PercentageDisplayFormatConfiguration](aws-properties-quicksight-dashboard-percentagedisplayformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)