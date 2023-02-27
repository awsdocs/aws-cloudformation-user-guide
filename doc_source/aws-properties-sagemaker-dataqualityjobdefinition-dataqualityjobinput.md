# AWS::SageMaker::DataQualityJobDefinition DataQualityJobInput<a name="aws-properties-sagemaker-dataqualityjobdefinition-dataqualityjobinput"></a>

The input for the data quality monitoring job\. Currently endpoints are supported for input\.

## Syntax<a name="aws-properties-sagemaker-dataqualityjobdefinition-dataqualityjobinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-dataqualityjobdefinition-dataqualityjobinput-syntax.json"></a>

```
{
  "[BatchTransformInput](#cfn-sagemaker-dataqualityjobdefinition-dataqualityjobinput-batchtransforminput)" : BatchTransformInput,
  "[EndpointInput](#cfn-sagemaker-dataqualityjobdefinition-dataqualityjobinput-endpointinput)" : EndpointInput
}
```

### YAML<a name="aws-properties-sagemaker-dataqualityjobdefinition-dataqualityjobinput-syntax.yaml"></a>

```
  [BatchTransformInput](#cfn-sagemaker-dataqualityjobdefinition-dataqualityjobinput-batchtransforminput): 
    BatchTransformInput
  [EndpointInput](#cfn-sagemaker-dataqualityjobdefinition-dataqualityjobinput-endpointinput): 
    EndpointInput
```

## Properties<a name="aws-properties-sagemaker-dataqualityjobdefinition-dataqualityjobinput-properties"></a>

`BatchTransformInput`  <a name="cfn-sagemaker-dataqualityjobdefinition-dataqualityjobinput-batchtransforminput"></a>
Property description not available\.  
*Required*: No  
*Type*: [BatchTransformInput](aws-properties-sagemaker-dataqualityjobdefinition-batchtransforminput.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EndpointInput`  <a name="cfn-sagemaker-dataqualityjobdefinition-dataqualityjobinput-endpointinput"></a>
Input object for the endpoint  
*Required*: No  
*Type*: [EndpointInput](aws-properties-sagemaker-dataqualityjobdefinition-endpointinput.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)