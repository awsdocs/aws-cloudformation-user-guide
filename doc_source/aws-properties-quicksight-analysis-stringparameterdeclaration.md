# AWS::QuickSight::Analysis StringParameterDeclaration<a name="aws-properties-quicksight-analysis-stringparameterdeclaration"></a>

A parameter declaration for the `String` data type\.

## Syntax<a name="aws-properties-quicksight-analysis-stringparameterdeclaration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-stringparameterdeclaration-syntax.json"></a>

```
{
  "[DefaultValues](#cfn-quicksight-analysis-stringparameterdeclaration-defaultvalues)" : StringDefaultValues,
  "[MappedDataSetParameters](#cfn-quicksight-analysis-stringparameterdeclaration-mappeddatasetparameters)" : [ MappedDataSetParameter, ... ],
  "[Name](#cfn-quicksight-analysis-stringparameterdeclaration-name)" : String,
  "[ParameterValueType](#cfn-quicksight-analysis-stringparameterdeclaration-parametervaluetype)" : String,
  "[ValueWhenUnset](#cfn-quicksight-analysis-stringparameterdeclaration-valuewhenunset)" : StringValueWhenUnsetConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-stringparameterdeclaration-syntax.yaml"></a>

```
  [DefaultValues](#cfn-quicksight-analysis-stringparameterdeclaration-defaultvalues): 
    StringDefaultValues
  [MappedDataSetParameters](#cfn-quicksight-analysis-stringparameterdeclaration-mappeddatasetparameters): 
    - MappedDataSetParameter
  [Name](#cfn-quicksight-analysis-stringparameterdeclaration-name): String
  [ParameterValueType](#cfn-quicksight-analysis-stringparameterdeclaration-parametervaluetype): String
  [ValueWhenUnset](#cfn-quicksight-analysis-stringparameterdeclaration-valuewhenunset): 
    StringValueWhenUnsetConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-stringparameterdeclaration-properties"></a>

`DefaultValues`  <a name="cfn-quicksight-analysis-stringparameterdeclaration-defaultvalues"></a>
The default values of a parameter\. If the parameter is a single\-value parameter, a maximum of one default value can be provided\.  
*Required*: No  
*Type*: [StringDefaultValues](aws-properties-quicksight-analysis-stringdefaultvalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MappedDataSetParameters`  <a name="cfn-quicksight-analysis-stringparameterdeclaration-mappeddatasetparameters"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [MappedDataSetParameter](aws-properties-quicksight-analysis-mappeddatasetparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-analysis-stringparameterdeclaration-name"></a>
The name of the parameter that is being declared\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterValueType`  <a name="cfn-quicksight-analysis-stringparameterdeclaration-parametervaluetype"></a>
The value type determines whether the parameter is a single\-value or multi\-value parameter\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `MULTI_VALUED | SINGLE_VALUED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueWhenUnset`  <a name="cfn-quicksight-analysis-stringparameterdeclaration-valuewhenunset"></a>
The configuration that defines the default value of a `String` parameter when a value has not been set\.  
*Required*: No  
*Type*: [StringValueWhenUnsetConfiguration](aws-properties-quicksight-analysis-stringvaluewhenunsetconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)