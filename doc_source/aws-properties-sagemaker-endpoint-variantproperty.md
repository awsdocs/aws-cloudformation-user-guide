# AWS::SageMaker::Endpoint VariantProperty<a name="aws-properties-sagemaker-endpoint-variantproperty"></a>

Specifies a production variant property type for an Endpoint\.

If you are updating an Endpoint with the [RetainAllVariantProperties](https://docs.aws.amazon.com/sagemaker/latest/dg/API_UpdateEndpoint.html#SageMaker-UpdateEndpoint-request-RetainAllVariantProperties) option set to `true`, the `VarientProperty` objects listed in [ExcludeRetainedVariantProperties](https://docs.aws.amazon.com/sagemaker/latest/dg/API_UpdateEndpoint.html#SageMaker-UpdateEndpoint-request-ExcludeRetainedVariantProperties) override the existing variant properties of the Endpoint\.

## Syntax<a name="aws-properties-sagemaker-endpoint-variantproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpoint-variantproperty-syntax.json"></a>

```
{
  "[VariantPropertyType](#cfn-sagemaker-endpoint-variantproperty-variantpropertytype)" : String
}
```

### YAML<a name="aws-properties-sagemaker-endpoint-variantproperty-syntax.yaml"></a>

```
  [VariantPropertyType](#cfn-sagemaker-endpoint-variantproperty-variantpropertytype): String
```

## Properties<a name="aws-properties-sagemaker-endpoint-variantproperty-properties"></a>

`VariantPropertyType`  <a name="cfn-sagemaker-endpoint-variantproperty-variantpropertytype"></a>
The type of variant property\. The supported values are:  
+ `DesiredInstanceCount`: Overrides the existing variant instance counts using the [InitialInstanceCount](https://docs.aws.amazon.com/sagemaker/latest/dg/API_ProductionVariant.html#SageMaker-Type-ProductionVariant-InitialInstanceCount) values in the [ProductionVariants](https://docs.aws.amazon.com/sagemaker/latest/dg/API_CreateEndpointConfig.html#SageMaker-CreateEndpointConfig-request-ProductionVariants)\.
+ `DesiredWeight`: Overrides the existing variant weights using the [InitialVariantWeight](https://docs.aws.amazon.com/sagemaker/latest/dg/API_ProductionVariant.html#SageMaker-Type-ProductionVariant-InitialVariantWeight) values in the [ProductionVariants](https://docs.aws.amazon.com/sagemaker/latest/dg/API_CreateEndpointConfig.html#SageMaker-CreateEndpointConfig-request-ProductionVariants)\.
+ `DataCaptureConfig`: \(Not currently supported\.\)
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)