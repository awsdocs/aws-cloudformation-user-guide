# AWS::Personalize::Solution ContinuousHyperParameterRange<a name="aws-properties-personalize-solution-continuoushyperparameterrange"></a>

Provides the name and range of a continuous hyperparameter\.

## Syntax<a name="aws-properties-personalize-solution-continuoushyperparameterrange-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-personalize-solution-continuoushyperparameterrange-syntax.json"></a>

```
{
  "[MaxValue](#cfn-personalize-solution-continuoushyperparameterrange-maxvalue)" : Double,
  "[MinValue](#cfn-personalize-solution-continuoushyperparameterrange-minvalue)" : Double,
  "[Name](#cfn-personalize-solution-continuoushyperparameterrange-name)" : String
}
```

### YAML<a name="aws-properties-personalize-solution-continuoushyperparameterrange-syntax.yaml"></a>

```
  [MaxValue](#cfn-personalize-solution-continuoushyperparameterrange-maxvalue): Double
  [MinValue](#cfn-personalize-solution-continuoushyperparameterrange-minvalue): Double
  [Name](#cfn-personalize-solution-continuoushyperparameterrange-name): String
```

## Properties<a name="aws-properties-personalize-solution-continuoushyperparameterrange-properties"></a>

`MaxValue`  <a name="cfn-personalize-solution-continuoushyperparameterrange-maxvalue"></a>
The maximum allowable value for the hyperparameter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MinValue`  <a name="cfn-personalize-solution-continuoushyperparameterrange-minvalue"></a>
The minimum allowable value for the hyperparameter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-personalize-solution-continuoushyperparameterrange-name"></a>
The name of the hyperparameter\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)