# AWS::QuickSight::Analysis CustomParameterValues<a name="aws-properties-quicksight-analysis-customparametervalues"></a>

The customized parameter values\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-customparametervalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-customparametervalues-syntax.json"></a>

```
{
  "[DateTimeValues](#cfn-quicksight-analysis-customparametervalues-datetimevalues)" : [ String, ... ],
  "[DecimalValues](#cfn-quicksight-analysis-customparametervalues-decimalvalues)" : [ Double, ... ],
  "[IntegerValues](#cfn-quicksight-analysis-customparametervalues-integervalues)" : [ Double, ... ],
  "[StringValues](#cfn-quicksight-analysis-customparametervalues-stringvalues)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-customparametervalues-syntax.yaml"></a>

```
  [DateTimeValues](#cfn-quicksight-analysis-customparametervalues-datetimevalues): 
    - String
  [DecimalValues](#cfn-quicksight-analysis-customparametervalues-decimalvalues): 
    - Double
  [IntegerValues](#cfn-quicksight-analysis-customparametervalues-integervalues): 
    - Double
  [StringValues](#cfn-quicksight-analysis-customparametervalues-stringvalues): 
    - String
```

## Properties<a name="aws-properties-quicksight-analysis-customparametervalues-properties"></a>

`DateTimeValues`  <a name="cfn-quicksight-analysis-customparametervalues-datetimevalues"></a>
A list of datetime\-type parameter values\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DecimalValues`  <a name="cfn-quicksight-analysis-customparametervalues-decimalvalues"></a>
A list of decimal\-type parameter values\.  
*Required*: No  
*Type*: List of Double  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegerValues`  <a name="cfn-quicksight-analysis-customparametervalues-integervalues"></a>
A list of integer\-type parameter values\.  
*Required*: No  
*Type*: List of Double  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringValues`  <a name="cfn-quicksight-analysis-customparametervalues-stringvalues"></a>
A list of string\-type parameter values\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)