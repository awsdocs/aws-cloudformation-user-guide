# AWS::SageMaker::InferenceExperiment EndpointMetadata<a name="aws-properties-sagemaker-inferenceexperiment-endpointmetadata"></a>

The metadata of the endpoint\.

## Syntax<a name="aws-properties-sagemaker-inferenceexperiment-endpointmetadata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-inferenceexperiment-endpointmetadata-syntax.json"></a>

```
{
  "[EndpointConfigName](#cfn-sagemaker-inferenceexperiment-endpointmetadata-endpointconfigname)" : String,
  "[EndpointName](#cfn-sagemaker-inferenceexperiment-endpointmetadata-endpointname)" : String,
  "[EndpointStatus](#cfn-sagemaker-inferenceexperiment-endpointmetadata-endpointstatus)" : String
}
```

### YAML<a name="aws-properties-sagemaker-inferenceexperiment-endpointmetadata-syntax.yaml"></a>

```
  [EndpointConfigName](#cfn-sagemaker-inferenceexperiment-endpointmetadata-endpointconfigname): String
  [EndpointName](#cfn-sagemaker-inferenceexperiment-endpointmetadata-endpointname): String
  [EndpointStatus](#cfn-sagemaker-inferenceexperiment-endpointmetadata-endpointstatus): String
```

## Properties<a name="aws-properties-sagemaker-inferenceexperiment-endpointmetadata-properties"></a>

`EndpointConfigName`  <a name="cfn-sagemaker-inferenceexperiment-endpointmetadata-endpointconfigname"></a>
The name of the endpoint configuration\.  
*Required*: No  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointName`  <a name="cfn-sagemaker-inferenceexperiment-endpointmetadata-endpointname"></a>
The name of the endpoint\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointStatus`  <a name="cfn-sagemaker-inferenceexperiment-endpointmetadata-endpointstatus"></a>
 The status of the endpoint\. For possible values of the status of an endpoint, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sagemaker-inferenceexperiment-endpointmetadata.html#cfn-sagemaker-inferenceexperiment-endpointmetadata-endpointstatus](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sagemaker-inferenceexperiment-endpointmetadata.html#cfn-sagemaker-inferenceexperiment-endpointmetadata-endpointstatus)\.   
*Required*: No  
*Type*: String  
*Allowed values*: `Creating | Deleting | Failed | InService | OutOfService | RollingBack | SystemUpdating | Updating`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)