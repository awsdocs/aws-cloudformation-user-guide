# AWS::SageMaker::EndpointConfig ClarifyShapConfig<a name="aws-properties-sagemaker-endpointconfig-clarifyshapconfig"></a>

<a name="aws-properties-sagemaker-endpointconfig-clarifyshapconfig-description"></a>The `ClarifyShapConfig` property type specifies Property description not available\. for an [AWS::SageMaker::EndpointConfig](aws-resource-sagemaker-endpointconfig.md)\.

## Syntax<a name="aws-properties-sagemaker-endpointconfig-clarifyshapconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpointconfig-clarifyshapconfig-syntax.json"></a>

```
{
  "[NumberOfSamples](#cfn-sagemaker-endpointconfig-clarifyshapconfig-numberofsamples)" : Integer,
  "[Seed](#cfn-sagemaker-endpointconfig-clarifyshapconfig-seed)" : Integer,
  "[ShapBaselineConfig](#cfn-sagemaker-endpointconfig-clarifyshapconfig-shapbaselineconfig)" : ClarifyShapBaselineConfig,
  "[TextConfig](#cfn-sagemaker-endpointconfig-clarifyshapconfig-textconfig)" : ClarifyTextConfig,
  "[UseLogit](#cfn-sagemaker-endpointconfig-clarifyshapconfig-uselogit)" : Boolean
}
```

### YAML<a name="aws-properties-sagemaker-endpointconfig-clarifyshapconfig-syntax.yaml"></a>

```
  [NumberOfSamples](#cfn-sagemaker-endpointconfig-clarifyshapconfig-numberofsamples): Integer
  [Seed](#cfn-sagemaker-endpointconfig-clarifyshapconfig-seed): Integer
  [ShapBaselineConfig](#cfn-sagemaker-endpointconfig-clarifyshapconfig-shapbaselineconfig): 
    ClarifyShapBaselineConfig
  [TextConfig](#cfn-sagemaker-endpointconfig-clarifyshapconfig-textconfig): 
    ClarifyTextConfig
  [UseLogit](#cfn-sagemaker-endpointconfig-clarifyshapconfig-uselogit): Boolean
```

## Properties<a name="aws-properties-sagemaker-endpointconfig-clarifyshapconfig-properties"></a>

`NumberOfSamples`  <a name="cfn-sagemaker-endpointconfig-clarifyshapconfig-numberofsamples"></a>
Property description not available\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Seed`  <a name="cfn-sagemaker-endpointconfig-clarifyshapconfig-seed"></a>
Property description not available\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ShapBaselineConfig`  <a name="cfn-sagemaker-endpointconfig-clarifyshapconfig-shapbaselineconfig"></a>
Property description not available\.  
*Required*: Yes  
*Type*: [ClarifyShapBaselineConfig](aws-properties-sagemaker-endpointconfig-clarifyshapbaselineconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TextConfig`  <a name="cfn-sagemaker-endpointconfig-clarifyshapconfig-textconfig"></a>
Property description not available\.  
*Required*: No  
*Type*: [ClarifyTextConfig](aws-properties-sagemaker-endpointconfig-clarifytextconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UseLogit`  <a name="cfn-sagemaker-endpointconfig-clarifyshapconfig-uselogit"></a>
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)