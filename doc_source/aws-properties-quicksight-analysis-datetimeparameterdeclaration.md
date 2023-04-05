# AWS::QuickSight::Analysis DateTimeParameterDeclaration<a name="aws-properties-quicksight-analysis-datetimeparameterdeclaration"></a>

A parameter declaration for the `DateTime` data type\.

## Syntax<a name="aws-properties-quicksight-analysis-datetimeparameterdeclaration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-datetimeparameterdeclaration-syntax.json"></a>

```
{
  "[DefaultValues](#cfn-quicksight-analysis-datetimeparameterdeclaration-defaultvalues)" : DateTimeDefaultValues,
  "[MappedDataSetParameters](#cfn-quicksight-analysis-datetimeparameterdeclaration-mappeddatasetparameters)" : [ MappedDataSetParameter, ... ],
  "[Name](#cfn-quicksight-analysis-datetimeparameterdeclaration-name)" : String,
  "[TimeGranularity](#cfn-quicksight-analysis-datetimeparameterdeclaration-timegranularity)" : String,
  "[ValueWhenUnset](#cfn-quicksight-analysis-datetimeparameterdeclaration-valuewhenunset)" : DateTimeValueWhenUnsetConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-datetimeparameterdeclaration-syntax.yaml"></a>

```
  [DefaultValues](#cfn-quicksight-analysis-datetimeparameterdeclaration-defaultvalues): 
    DateTimeDefaultValues
  [MappedDataSetParameters](#cfn-quicksight-analysis-datetimeparameterdeclaration-mappeddatasetparameters): 
    - MappedDataSetParameter
  [Name](#cfn-quicksight-analysis-datetimeparameterdeclaration-name): String
  [TimeGranularity](#cfn-quicksight-analysis-datetimeparameterdeclaration-timegranularity): String
  [ValueWhenUnset](#cfn-quicksight-analysis-datetimeparameterdeclaration-valuewhenunset): 
    DateTimeValueWhenUnsetConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-datetimeparameterdeclaration-properties"></a>

`DefaultValues`  <a name="cfn-quicksight-analysis-datetimeparameterdeclaration-defaultvalues"></a>
The default values of a parameter\. If the parameter is a single\-value parameter, a maximum of one default value can be provided\.  
*Required*: No  
*Type*: [DateTimeDefaultValues](aws-properties-quicksight-analysis-datetimedefaultvalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MappedDataSetParameters`  <a name="cfn-quicksight-analysis-datetimeparameterdeclaration-mappeddatasetparameters"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [MappedDataSetParameter](aws-properties-quicksight-analysis-mappeddatasetparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-analysis-datetimeparameterdeclaration-name"></a>
The name of the parameter that is being declared\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeGranularity`  <a name="cfn-quicksight-analysis-datetimeparameterdeclaration-timegranularity"></a>
The level of time precision that is used to aggregate `DateTime` values\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DAY | HOUR | MILLISECOND | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueWhenUnset`  <a name="cfn-quicksight-analysis-datetimeparameterdeclaration-valuewhenunset"></a>
The configuration that defines the default value of a `DateTime` parameter when a value has not been set\.  
*Required*: No  
*Type*: [DateTimeValueWhenUnsetConfiguration](aws-properties-quicksight-analysis-datetimevaluewhenunsetconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)