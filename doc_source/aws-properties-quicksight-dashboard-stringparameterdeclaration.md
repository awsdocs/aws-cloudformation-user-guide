# AWS::QuickSight::Dashboard StringParameterDeclaration<a name="aws-properties-quicksight-dashboard-stringparameterdeclaration"></a>

A parameter declaration for the `String` data type\.

## Syntax<a name="aws-properties-quicksight-dashboard-stringparameterdeclaration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-stringparameterdeclaration-syntax.json"></a>

```
{
  "[DefaultValues](#cfn-quicksight-dashboard-stringparameterdeclaration-defaultvalues)" : StringDefaultValues,
  "[MappedDataSetParameters](#cfn-quicksight-dashboard-stringparameterdeclaration-mappeddatasetparameters)" : [ MappedDataSetParameter, ... ],
  "[Name](#cfn-quicksight-dashboard-stringparameterdeclaration-name)" : String,
  "[ParameterValueType](#cfn-quicksight-dashboard-stringparameterdeclaration-parametervaluetype)" : String,
  "[ValueWhenUnset](#cfn-quicksight-dashboard-stringparameterdeclaration-valuewhenunset)" : StringValueWhenUnsetConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-stringparameterdeclaration-syntax.yaml"></a>

```
  [DefaultValues](#cfn-quicksight-dashboard-stringparameterdeclaration-defaultvalues): 
    StringDefaultValues
  [MappedDataSetParameters](#cfn-quicksight-dashboard-stringparameterdeclaration-mappeddatasetparameters): 
    - MappedDataSetParameter
  [Name](#cfn-quicksight-dashboard-stringparameterdeclaration-name): String
  [ParameterValueType](#cfn-quicksight-dashboard-stringparameterdeclaration-parametervaluetype): String
  [ValueWhenUnset](#cfn-quicksight-dashboard-stringparameterdeclaration-valuewhenunset): 
    StringValueWhenUnsetConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-stringparameterdeclaration-properties"></a>

`DefaultValues`  <a name="cfn-quicksight-dashboard-stringparameterdeclaration-defaultvalues"></a>
The default values of a parameter\. If the parameter is a single\-value parameter, a maximum of one default value can be provided\.  
*Required*: No  
*Type*: [StringDefaultValues](aws-properties-quicksight-dashboard-stringdefaultvalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MappedDataSetParameters`  <a name="cfn-quicksight-dashboard-stringparameterdeclaration-mappeddatasetparameters"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [MappedDataSetParameter](aws-properties-quicksight-dashboard-mappeddatasetparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-dashboard-stringparameterdeclaration-name"></a>
The name of the parameter that is being declared\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterValueType`  <a name="cfn-quicksight-dashboard-stringparameterdeclaration-parametervaluetype"></a>
The value type determines whether the parameter is a single\-value or multi\-value parameter\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `MULTI_VALUED | SINGLE_VALUED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueWhenUnset`  <a name="cfn-quicksight-dashboard-stringparameterdeclaration-valuewhenunset"></a>
The configuration that defines the default value of a `String` parameter when a value has not been set\.  
*Required*: No  
*Type*: [StringValueWhenUnsetConfiguration](aws-properties-quicksight-dashboard-stringvaluewhenunsetconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)