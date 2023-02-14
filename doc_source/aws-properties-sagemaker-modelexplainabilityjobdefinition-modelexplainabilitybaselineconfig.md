# AWS::SageMaker::ModelExplainabilityJobDefinition ModelExplainabilityBaselineConfig<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-modelexplainabilitybaselineconfig"></a>

The configuration for a baseline model explainability job\.

## Syntax<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-modelexplainabilitybaselineconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-modelexplainabilitybaselineconfig-syntax.json"></a>

```
{
  "[BaseliningJobName](#cfn-sagemaker-modelexplainabilityjobdefinition-modelexplainabilitybaselineconfig-baseliningjobname)" : String,
  "[ConstraintsResource](#cfn-sagemaker-modelexplainabilityjobdefinition-modelexplainabilitybaselineconfig-constraintsresource)" : ConstraintsResource
}
```

### YAML<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-modelexplainabilitybaselineconfig-syntax.yaml"></a>

```
  [BaseliningJobName](#cfn-sagemaker-modelexplainabilityjobdefinition-modelexplainabilitybaselineconfig-baseliningjobname): String
  [ConstraintsResource](#cfn-sagemaker-modelexplainabilityjobdefinition-modelexplainabilitybaselineconfig-constraintsresource): 
    ConstraintsResource
```

## Properties<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-modelexplainabilitybaselineconfig-properties"></a>

`BaseliningJobName`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-modelexplainabilitybaselineconfig-baseliningjobname"></a>
The name of the baseline model explainability job\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConstraintsResource`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-modelexplainabilitybaselineconfig-constraintsresource"></a>
The constraints resource for a model explainability job\.   
*Required*: No  
*Type*: [ConstraintsResource](aws-properties-sagemaker-modelexplainabilityjobdefinition-constraintsresource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)