# AWS::QuickSight::Analysis DecimalParameter<a name="aws-properties-quicksight-analysis-decimalparameter"></a>

A decimal parameter\.

## Syntax<a name="aws-properties-quicksight-analysis-decimalparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-decimalparameter-syntax.json"></a>

```
{
  "[Name](#cfn-quicksight-analysis-decimalparameter-name)" : String,
  "[Values](#cfn-quicksight-analysis-decimalparameter-values)" : [ Double, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-decimalparameter-syntax.yaml"></a>

```
  [Name](#cfn-quicksight-analysis-decimalparameter-name): String
  [Values](#cfn-quicksight-analysis-decimalparameter-values): 
    - Double
```

## Properties<a name="aws-properties-quicksight-analysis-decimalparameter-properties"></a>

`Name`  <a name="cfn-quicksight-analysis-decimalparameter-name"></a>
A display name for the decimal parameter\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-analysis-decimalparameter-values"></a>
The values for the decimal parameter\.  
*Required*: Yes  
*Type*: List of Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)