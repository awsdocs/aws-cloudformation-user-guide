# AWS::QuickSight::Template ComparisonFormatConfiguration<a name="aws-properties-quicksight-template-comparisonformatconfiguration"></a>

The format of the comparison\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-comparisonformatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-comparisonformatconfiguration-syntax.json"></a>

```
{
  "[NumberDisplayFormatConfiguration](#cfn-quicksight-template-comparisonformatconfiguration-numberdisplayformatconfiguration)" : NumberDisplayFormatConfiguration,
  "[PercentageDisplayFormatConfiguration](#cfn-quicksight-template-comparisonformatconfiguration-percentagedisplayformatconfiguration)" : PercentageDisplayFormatConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-comparisonformatconfiguration-syntax.yaml"></a>

```
  [NumberDisplayFormatConfiguration](#cfn-quicksight-template-comparisonformatconfiguration-numberdisplayformatconfiguration): 
    NumberDisplayFormatConfiguration
  [PercentageDisplayFormatConfiguration](#cfn-quicksight-template-comparisonformatconfiguration-percentagedisplayformatconfiguration): 
    PercentageDisplayFormatConfiguration
```

## Properties<a name="aws-properties-quicksight-template-comparisonformatconfiguration-properties"></a>

`NumberDisplayFormatConfiguration`  <a name="cfn-quicksight-template-comparisonformatconfiguration-numberdisplayformatconfiguration"></a>
The number display format\.  
*Required*: No  
*Type*: [NumberDisplayFormatConfiguration](aws-properties-quicksight-template-numberdisplayformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PercentageDisplayFormatConfiguration`  <a name="cfn-quicksight-template-comparisonformatconfiguration-percentagedisplayformatconfiguration"></a>
The percentage display format\.  
*Required*: No  
*Type*: [PercentageDisplayFormatConfiguration](aws-properties-quicksight-template-percentagedisplayformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)