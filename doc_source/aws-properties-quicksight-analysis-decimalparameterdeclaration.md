# AWS::QuickSight::Analysis DecimalParameterDeclaration<a name="aws-properties-quicksight-analysis-decimalparameterdeclaration"></a>

A parameter declaration for the `Decimal` data type\.

## Syntax<a name="aws-properties-quicksight-analysis-decimalparameterdeclaration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-decimalparameterdeclaration-syntax.json"></a>

```
{
  "[DefaultValues](#cfn-quicksight-analysis-decimalparameterdeclaration-defaultvalues)" : DecimalDefaultValues,
  "[MappedDataSetParameters](#cfn-quicksight-analysis-decimalparameterdeclaration-mappeddatasetparameters)" : [ MappedDataSetParameter, ... ],
  "[Name](#cfn-quicksight-analysis-decimalparameterdeclaration-name)" : String,
  "[ParameterValueType](#cfn-quicksight-analysis-decimalparameterdeclaration-parametervaluetype)" : String,
  "[ValueWhenUnset](#cfn-quicksight-analysis-decimalparameterdeclaration-valuewhenunset)" : DecimalValueWhenUnsetConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-decimalparameterdeclaration-syntax.yaml"></a>

```
  [DefaultValues](#cfn-quicksight-analysis-decimalparameterdeclaration-defaultvalues): 
    DecimalDefaultValues
  [MappedDataSetParameters](#cfn-quicksight-analysis-decimalparameterdeclaration-mappeddatasetparameters): 
    - MappedDataSetParameter
  [Name](#cfn-quicksight-analysis-decimalparameterdeclaration-name): String
  [ParameterValueType](#cfn-quicksight-analysis-decimalparameterdeclaration-parametervaluetype): String
  [ValueWhenUnset](#cfn-quicksight-analysis-decimalparameterdeclaration-valuewhenunset): 
    DecimalValueWhenUnsetConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-decimalparameterdeclaration-properties"></a>

`DefaultValues`  <a name="cfn-quicksight-analysis-decimalparameterdeclaration-defaultvalues"></a>
The default values of a parameter\. If the parameter is a single\-value parameter, a maximum of one default value can be provided\.  
*Required*: No  
*Type*: [DecimalDefaultValues](aws-properties-quicksight-analysis-decimaldefaultvalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MappedDataSetParameters`  <a name="cfn-quicksight-analysis-decimalparameterdeclaration-mappeddatasetparameters"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [MappedDataSetParameter](aws-properties-quicksight-analysis-mappeddatasetparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-analysis-decimalparameterdeclaration-name"></a>
The name of the parameter that is being declared\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterValueType`  <a name="cfn-quicksight-analysis-decimalparameterdeclaration-parametervaluetype"></a>
The value type determines whether the parameter is a single\-value or multi\-value parameter\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `MULTI_VALUED | SINGLE_VALUED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueWhenUnset`  <a name="cfn-quicksight-analysis-decimalparameterdeclaration-valuewhenunset"></a>
The configuration that defines the default value of a `Decimal` parameter when a value has not been set\.  
*Required*: No  
*Type*: [DecimalValueWhenUnsetConfiguration](aws-properties-quicksight-analysis-decimalvaluewhenunsetconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)