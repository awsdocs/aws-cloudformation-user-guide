# AWS::QuickSight::Dashboard IntegerParameter<a name="aws-properties-quicksight-dashboard-integerparameter"></a>

An integer parameter\.

## Syntax<a name="aws-properties-quicksight-dashboard-integerparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-integerparameter-syntax.json"></a>

```
{
  "[Name](#cfn-quicksight-dashboard-integerparameter-name)" : String,
  "[Values](#cfn-quicksight-dashboard-integerparameter-values)" : [ Double, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-integerparameter-syntax.yaml"></a>

```
  [Name](#cfn-quicksight-dashboard-integerparameter-name): String
  [Values](#cfn-quicksight-dashboard-integerparameter-values): 
    - Double
```

## Properties<a name="aws-properties-quicksight-dashboard-integerparameter-properties"></a>

`Name`  <a name="cfn-quicksight-dashboard-integerparameter-name"></a>
The name of the integer parameter\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-dashboard-integerparameter-values"></a>
The values for the integer parameter\.  
*Required*: Yes  
*Type*: List of Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)