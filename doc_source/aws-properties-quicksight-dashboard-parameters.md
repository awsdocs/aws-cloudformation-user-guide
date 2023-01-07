# AWS::QuickSight::Dashboard Parameters<a name="aws-properties-quicksight-dashboard-parameters"></a>

A list of Amazon QuickSight parameters and the list's override values\.

## Syntax<a name="aws-properties-quicksight-dashboard-parameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-parameters-syntax.json"></a>

```
{
  "[DateTimeParameters](#cfn-quicksight-dashboard-parameters-datetimeparameters)" : [ DateTimeParameter, ... ],
  "[DecimalParameters](#cfn-quicksight-dashboard-parameters-decimalparameters)" : [ DecimalParameter, ... ],
  "[IntegerParameters](#cfn-quicksight-dashboard-parameters-integerparameters)" : [ IntegerParameter, ... ],
  "[StringParameters](#cfn-quicksight-dashboard-parameters-stringparameters)" : [ StringParameter, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-parameters-syntax.yaml"></a>

```
  [DateTimeParameters](#cfn-quicksight-dashboard-parameters-datetimeparameters): 
    - DateTimeParameter
  [DecimalParameters](#cfn-quicksight-dashboard-parameters-decimalparameters): 
    - DecimalParameter
  [IntegerParameters](#cfn-quicksight-dashboard-parameters-integerparameters): 
    - IntegerParameter
  [StringParameters](#cfn-quicksight-dashboard-parameters-stringparameters): 
    - StringParameter
```

## Properties<a name="aws-properties-quicksight-dashboard-parameters-properties"></a>

`DateTimeParameters`  <a name="cfn-quicksight-dashboard-parameters-datetimeparameters"></a>
The parameters that have a data type of date\-time\.  
*Required*: No  
*Type*: List of [DateTimeParameter](aws-properties-quicksight-dashboard-datetimeparameter.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DecimalParameters`  <a name="cfn-quicksight-dashboard-parameters-decimalparameters"></a>
The parameters that have a data type of decimal\.  
*Required*: No  
*Type*: List of [DecimalParameter](aws-properties-quicksight-dashboard-decimalparameter.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegerParameters`  <a name="cfn-quicksight-dashboard-parameters-integerparameters"></a>
The parameters that have a data type of integer\.  
*Required*: No  
*Type*: List of [IntegerParameter](aws-properties-quicksight-dashboard-integerparameter.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringParameters`  <a name="cfn-quicksight-dashboard-parameters-stringparameters"></a>
The parameters that have a data type of string\.  
*Required*: No  
*Type*: List of [StringParameter](aws-properties-quicksight-dashboard-stringparameter.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)