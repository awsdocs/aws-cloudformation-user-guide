# AWS::QuickSight::Template CustomValuesConfiguration<a name="aws-properties-quicksight-template-customvaluesconfiguration"></a>

The configuration of custom values for the destination parameter in `DestinationParameterValueConfiguration`\.

## Syntax<a name="aws-properties-quicksight-template-customvaluesconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-customvaluesconfiguration-syntax.json"></a>

```
{
  "[CustomValues](#cfn-quicksight-template-customvaluesconfiguration-customvalues)" : CustomParameterValues,
  "[IncludeNullValue](#cfn-quicksight-template-customvaluesconfiguration-includenullvalue)" : Boolean
}
```

### YAML<a name="aws-properties-quicksight-template-customvaluesconfiguration-syntax.yaml"></a>

```
  [CustomValues](#cfn-quicksight-template-customvaluesconfiguration-customvalues): 
    CustomParameterValues
  [IncludeNullValue](#cfn-quicksight-template-customvaluesconfiguration-includenullvalue): Boolean
```

## Properties<a name="aws-properties-quicksight-template-customvaluesconfiguration-properties"></a>

`CustomValues`  <a name="cfn-quicksight-template-customvaluesconfiguration-customvalues"></a>
Property description not available\.  
*Required*: Yes  
*Type*: [CustomParameterValues](aws-properties-quicksight-template-customparametervalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeNullValue`  <a name="cfn-quicksight-template-customvaluesconfiguration-includenullvalue"></a>
Includes the null value in custom action parameter values\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)