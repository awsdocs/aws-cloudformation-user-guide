# AWS::SageMaker::ModelBiasJobDefinition ModelBiasBaselineConfig<a name="aws-properties-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig"></a>

The configuration for a baseline model bias job\.

## Syntax<a name="aws-properties-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig-syntax.json"></a>

```
{
  "[BaseliningJobName](#cfn-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig-baseliningjobname)" : String,
  "[ConstraintsResource](#cfn-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig-constraintsresource)" : ConstraintsResource
}
```

### YAML<a name="aws-properties-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig-syntax.yaml"></a>

```
  [BaseliningJobName](#cfn-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig-baseliningjobname): String
  [ConstraintsResource](#cfn-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig-constraintsresource): 
    ConstraintsResource
```

## Properties<a name="aws-properties-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig-properties"></a>

`BaseliningJobName`  <a name="cfn-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig-baseliningjobname"></a>
The name of the baseline model bias job\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConstraintsResource`  <a name="cfn-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig-constraintsresource"></a>
The constraints resource for a monitoring job\.  
*Required*: No  
*Type*: [ConstraintsResource](aws-properties-sagemaker-modelbiasjobdefinition-constraintsresource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)