# AWS::SageMaker::ModelBiasJobDefinition ModelBiasJobInput<a name="aws-properties-sagemaker-modelbiasjobdefinition-modelbiasjobinput"></a>

Inputs for the model bias job\.

## Syntax<a name="aws-properties-sagemaker-modelbiasjobdefinition-modelbiasjobinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelbiasjobdefinition-modelbiasjobinput-syntax.json"></a>

```
{
  "[EndpointInput](#cfn-sagemaker-modelbiasjobdefinition-modelbiasjobinput-endpointinput)" : EndpointInput,
  "[GroundTruthS3Input](#cfn-sagemaker-modelbiasjobdefinition-modelbiasjobinput-groundtruths3input)" : MonitoringGroundTruthS3Input
}
```

### YAML<a name="aws-properties-sagemaker-modelbiasjobdefinition-modelbiasjobinput-syntax.yaml"></a>

```
  [EndpointInput](#cfn-sagemaker-modelbiasjobdefinition-modelbiasjobinput-endpointinput): 
    EndpointInput
  [GroundTruthS3Input](#cfn-sagemaker-modelbiasjobdefinition-modelbiasjobinput-groundtruths3input): 
    MonitoringGroundTruthS3Input
```

## Properties<a name="aws-properties-sagemaker-modelbiasjobdefinition-modelbiasjobinput-properties"></a>

`EndpointInput`  <a name="cfn-sagemaker-modelbiasjobdefinition-modelbiasjobinput-endpointinput"></a>
Input object for the endpoint\.  
*Required*: Yes  
*Type*: [EndpointInput](aws-properties-sagemaker-modelbiasjobdefinition-endpointinput.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroundTruthS3Input`  <a name="cfn-sagemaker-modelbiasjobdefinition-modelbiasjobinput-groundtruths3input"></a>
Location of ground truth labels to use in model bias job\.  
*Required*: Yes  
*Type*: [MonitoringGroundTruthS3Input](aws-properties-sagemaker-modelbiasjobdefinition-monitoringgroundtruths3input.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)