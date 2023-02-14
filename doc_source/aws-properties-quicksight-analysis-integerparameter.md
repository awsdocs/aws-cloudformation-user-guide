# AWS::QuickSight::Analysis IntegerParameter<a name="aws-properties-quicksight-analysis-integerparameter"></a>

An integer parameter\.

## Syntax<a name="aws-properties-quicksight-analysis-integerparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-integerparameter-syntax.json"></a>

```
{
  "[Name](#cfn-quicksight-analysis-integerparameter-name)" : String,
  "[Values](#cfn-quicksight-analysis-integerparameter-values)" : [ Double, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-integerparameter-syntax.yaml"></a>

```
  [Name](#cfn-quicksight-analysis-integerparameter-name): String
  [Values](#cfn-quicksight-analysis-integerparameter-values): 
    - Double
```

## Properties<a name="aws-properties-quicksight-analysis-integerparameter-properties"></a>

`Name`  <a name="cfn-quicksight-analysis-integerparameter-name"></a>
The name of the integer parameter\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-analysis-integerparameter-values"></a>
The values for the integer parameter\.  
*Required*: Yes  
*Type*: List of Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)