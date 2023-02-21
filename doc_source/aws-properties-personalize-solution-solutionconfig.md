# AWS::Personalize::Solution SolutionConfig<a name="aws-properties-personalize-solution-solutionconfig"></a>

Describes the configuration properties for the solution\.

## Syntax<a name="aws-properties-personalize-solution-solutionconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-personalize-solution-solutionconfig-syntax.json"></a>

```
{
  "[AlgorithmHyperParameters](#cfn-personalize-solution-solutionconfig-algorithmhyperparameters)" : {Key : Value, ...},
  "[AutoMLConfig](#cfn-personalize-solution-solutionconfig-automlconfig)" : AutoMLConfig,
  "[EventValueThreshold](#cfn-personalize-solution-solutionconfig-eventvaluethreshold)" : String,
  "[FeatureTransformationParameters](#cfn-personalize-solution-solutionconfig-featuretransformationparameters)" : {Key : Value, ...},
  "[HpoConfig](#cfn-personalize-solution-solutionconfig-hpoconfig)" : HpoConfig
}
```

### YAML<a name="aws-properties-personalize-solution-solutionconfig-syntax.yaml"></a>

```
  [AlgorithmHyperParameters](#cfn-personalize-solution-solutionconfig-algorithmhyperparameters): 
    Key : Value
  [AutoMLConfig](#cfn-personalize-solution-solutionconfig-automlconfig): 
    AutoMLConfig
  [EventValueThreshold](#cfn-personalize-solution-solutionconfig-eventvaluethreshold): String
  [FeatureTransformationParameters](#cfn-personalize-solution-solutionconfig-featuretransformationparameters): 
    Key : Value
  [HpoConfig](#cfn-personalize-solution-solutionconfig-hpoconfig): 
    HpoConfig
```

## Properties<a name="aws-properties-personalize-solution-solutionconfig-properties"></a>

`AlgorithmHyperParameters`  <a name="cfn-personalize-solution-solutionconfig-algorithmhyperparameters"></a>
Lists the hyperparameter names and ranges\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AutoMLConfig`  <a name="cfn-personalize-solution-solutionconfig-automlconfig"></a>
The [AutoMLConfig](https://docs.aws.amazon.com/personalize/latest/dg/API_AutoMLConfig.html) object containing a list of recipes to search when AutoML is performed\.  
*Required*: No  
*Type*: [AutoMLConfig](aws-properties-personalize-solution-automlconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EventValueThreshold`  <a name="cfn-personalize-solution-solutionconfig-eventvaluethreshold"></a>
Only events with a value greater than or equal to this threshold are used for training a model\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FeatureTransformationParameters`  <a name="cfn-personalize-solution-solutionconfig-featuretransformationparameters"></a>
Lists the feature transformation parameters\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HpoConfig`  <a name="cfn-personalize-solution-solutionconfig-hpoconfig"></a>
Describes the properties for hyperparameter optimization \(HPO\)\.  
*Required*: No  
*Type*: [HpoConfig](aws-properties-personalize-solution-hpoconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)