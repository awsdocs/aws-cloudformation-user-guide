# AWS::SageMaker::ModelQualityJobDefinition ModelQualityJobInput<a name="aws-properties-sagemaker-modelqualityjobdefinition-modelqualityjobinput"></a>

The input for the model quality monitoring job\. Currently endponts are supported for input for model quality monitoring jobs\.

## Syntax<a name="aws-properties-sagemaker-modelqualityjobdefinition-modelqualityjobinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelqualityjobdefinition-modelqualityjobinput-syntax.json"></a>

```
{
  "[EndpointInput](#cfn-sagemaker-modelqualityjobdefinition-modelqualityjobinput-endpointinput)" : EndpointInput,
  "[GroundTruthS3Input](#cfn-sagemaker-modelqualityjobdefinition-modelqualityjobinput-groundtruths3input)" : MonitoringGroundTruthS3Input
}
```

### YAML<a name="aws-properties-sagemaker-modelqualityjobdefinition-modelqualityjobinput-syntax.yaml"></a>

```
  [EndpointInput](#cfn-sagemaker-modelqualityjobdefinition-modelqualityjobinput-endpointinput): 
    EndpointInput
  [GroundTruthS3Input](#cfn-sagemaker-modelqualityjobdefinition-modelqualityjobinput-groundtruths3input): 
    MonitoringGroundTruthS3Input
```

## Properties<a name="aws-properties-sagemaker-modelqualityjobdefinition-modelqualityjobinput-properties"></a>

`EndpointInput`  <a name="cfn-sagemaker-modelqualityjobdefinition-modelqualityjobinput-endpointinput"></a>
Input object for the endpoint  
*Required*: Yes  
*Type*: [EndpointInput](aws-properties-sagemaker-modelqualityjobdefinition-endpointinput.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GroundTruthS3Input`  <a name="cfn-sagemaker-modelqualityjobdefinition-modelqualityjobinput-groundtruths3input"></a>
The ground truth label provided for the model\.  
*Required*: Yes  
*Type*: [MonitoringGroundTruthS3Input](aws-properties-sagemaker-modelqualityjobdefinition-monitoringgroundtruths3input.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)