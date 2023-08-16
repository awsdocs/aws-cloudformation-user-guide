# AWS::QuickSight::Template CustomParameterValues<a name="aws-properties-quicksight-template-customparametervalues"></a>

The customized parameter values\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-customparametervalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-customparametervalues-syntax.json"></a>

```
{
  "[DateTimeValues](#cfn-quicksight-template-customparametervalues-datetimevalues)" : [ String, ... ],
  "[DecimalValues](#cfn-quicksight-template-customparametervalues-decimalvalues)" : [ Double, ... ],
  "[IntegerValues](#cfn-quicksight-template-customparametervalues-integervalues)" : [ Double, ... ],
  "[StringValues](#cfn-quicksight-template-customparametervalues-stringvalues)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-customparametervalues-syntax.yaml"></a>

```
  [DateTimeValues](#cfn-quicksight-template-customparametervalues-datetimevalues): 
    - String
  [DecimalValues](#cfn-quicksight-template-customparametervalues-decimalvalues): 
    - Double
  [IntegerValues](#cfn-quicksight-template-customparametervalues-integervalues): 
    - Double
  [StringValues](#cfn-quicksight-template-customparametervalues-stringvalues): 
    - String
```

## Properties<a name="aws-properties-quicksight-template-customparametervalues-properties"></a>

`DateTimeValues`  <a name="cfn-quicksight-template-customparametervalues-datetimevalues"></a>
A list of datetime\-type parameter values\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DecimalValues`  <a name="cfn-quicksight-template-customparametervalues-decimalvalues"></a>
A list of decimal\-type parameter values\.  
*Required*: No  
*Type*: List of Double  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegerValues`  <a name="cfn-quicksight-template-customparametervalues-integervalues"></a>
A list of integer\-type parameter values\.  
*Required*: No  
*Type*: List of Double  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringValues`  <a name="cfn-quicksight-template-customparametervalues-stringvalues"></a>
A list of string\-type parameter values\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)