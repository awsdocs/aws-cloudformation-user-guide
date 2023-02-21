# AWS::SageMaker::EndpointConfig ClarifyExplainerConfig<a name="aws-properties-sagemaker-endpointconfig-clarifyexplainerconfig"></a>

<a name="aws-properties-sagemaker-endpointconfig-clarifyexplainerconfig-description"></a>The `ClarifyExplainerConfig` property type specifies Property description not available\. for an [AWS::SageMaker::EndpointConfig](aws-resource-sagemaker-endpointconfig.md)\.

## Syntax<a name="aws-properties-sagemaker-endpointconfig-clarifyexplainerconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpointconfig-clarifyexplainerconfig-syntax.json"></a>

```
{
  "[EnableExplanations](#cfn-sagemaker-endpointconfig-clarifyexplainerconfig-enableexplanations)" : String,
  "[InferenceConfig](#cfn-sagemaker-endpointconfig-clarifyexplainerconfig-inferenceconfig)" : ClarifyInferenceConfig,
  "[ShapConfig](#cfn-sagemaker-endpointconfig-clarifyexplainerconfig-shapconfig)" : ClarifyShapConfig
}
```

### YAML<a name="aws-properties-sagemaker-endpointconfig-clarifyexplainerconfig-syntax.yaml"></a>

```
  [EnableExplanations](#cfn-sagemaker-endpointconfig-clarifyexplainerconfig-enableexplanations): String
  [InferenceConfig](#cfn-sagemaker-endpointconfig-clarifyexplainerconfig-inferenceconfig): 
    ClarifyInferenceConfig
  [ShapConfig](#cfn-sagemaker-endpointconfig-clarifyexplainerconfig-shapconfig): 
    ClarifyShapConfig
```

## Properties<a name="aws-properties-sagemaker-endpointconfig-clarifyexplainerconfig-properties"></a>

`EnableExplanations`  <a name="cfn-sagemaker-endpointconfig-clarifyexplainerconfig-enableexplanations"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InferenceConfig`  <a name="cfn-sagemaker-endpointconfig-clarifyexplainerconfig-inferenceconfig"></a>
Property description not available\.  
*Required*: No  
*Type*: [ClarifyInferenceConfig](aws-properties-sagemaker-endpointconfig-clarifyinferenceconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ShapConfig`  <a name="cfn-sagemaker-endpointconfig-clarifyexplainerconfig-shapconfig"></a>
Property description not available\.  
*Required*: Yes  
*Type*: [ClarifyShapConfig](aws-properties-sagemaker-endpointconfig-clarifyshapconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)