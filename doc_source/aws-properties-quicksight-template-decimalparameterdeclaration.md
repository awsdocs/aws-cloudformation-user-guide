# AWS::QuickSight::Template DecimalParameterDeclaration<a name="aws-properties-quicksight-template-decimalparameterdeclaration"></a>

A parameter declaration for the `Decimal` data type\.

## Syntax<a name="aws-properties-quicksight-template-decimalparameterdeclaration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-decimalparameterdeclaration-syntax.json"></a>

```
{
  "[DefaultValues](#cfn-quicksight-template-decimalparameterdeclaration-defaultvalues)" : DecimalDefaultValues,
  "[MappedDataSetParameters](#cfn-quicksight-template-decimalparameterdeclaration-mappeddatasetparameters)" : [ MappedDataSetParameter, ... ],
  "[Name](#cfn-quicksight-template-decimalparameterdeclaration-name)" : String,
  "[ParameterValueType](#cfn-quicksight-template-decimalparameterdeclaration-parametervaluetype)" : String,
  "[ValueWhenUnset](#cfn-quicksight-template-decimalparameterdeclaration-valuewhenunset)" : DecimalValueWhenUnsetConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-decimalparameterdeclaration-syntax.yaml"></a>

```
  [DefaultValues](#cfn-quicksight-template-decimalparameterdeclaration-defaultvalues): 
    DecimalDefaultValues
  [MappedDataSetParameters](#cfn-quicksight-template-decimalparameterdeclaration-mappeddatasetparameters): 
    - MappedDataSetParameter
  [Name](#cfn-quicksight-template-decimalparameterdeclaration-name): String
  [ParameterValueType](#cfn-quicksight-template-decimalparameterdeclaration-parametervaluetype): String
  [ValueWhenUnset](#cfn-quicksight-template-decimalparameterdeclaration-valuewhenunset): 
    DecimalValueWhenUnsetConfiguration
```

## Properties<a name="aws-properties-quicksight-template-decimalparameterdeclaration-properties"></a>

`DefaultValues`  <a name="cfn-quicksight-template-decimalparameterdeclaration-defaultvalues"></a>
The default values of a parameter\. If the parameter is a single\-value parameter, a maximum of one default value can be provided\.  
*Required*: No  
*Type*: [DecimalDefaultValues](aws-properties-quicksight-template-decimaldefaultvalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MappedDataSetParameters`  <a name="cfn-quicksight-template-decimalparameterdeclaration-mappeddatasetparameters"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [MappedDataSetParameter](aws-properties-quicksight-template-mappeddatasetparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-template-decimalparameterdeclaration-name"></a>
The name of the parameter that is being declared\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterValueType`  <a name="cfn-quicksight-template-decimalparameterdeclaration-parametervaluetype"></a>
The value type determines whether the parameter is a single\-value or multi\-value parameter\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `MULTI_VALUED | SINGLE_VALUED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueWhenUnset`  <a name="cfn-quicksight-template-decimalparameterdeclaration-valuewhenunset"></a>
The configuration that defines the default value of a `Decimal` parameter when a value has not been set\.  
*Required*: No  
*Type*: [DecimalValueWhenUnsetConfiguration](aws-properties-quicksight-template-decimalvaluewhenunsetconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)