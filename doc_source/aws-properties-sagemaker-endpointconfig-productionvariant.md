# Amazon SageMaker EndpointConfig ProductionVariant<a name="aws-properties-sagemaker-endpointconfig-productionvariant"></a>

<a name="aws-properties-sagemaker-endpointconfig-productionvariant-description"></a>The `ProductionVariant` property type specifies a model that you want to host and the resources to deploy for hosting it\. If you are deploying multiple models, tell Amazon SageMaker how to distribute traffic among the models by specifying variant weights\.

<a name="aws-properties-sagemaker-endpointconfig-productionvariant-inheritance"></a> `ProductionVariant` is a property of the [AWS::SageMaker::EndpointConfig](aws-resource-sagemaker-endpointconfig.md) resource\.

## Syntax<a name="aws-properties-sagemaker-endpointconfig-productionvariant-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpointconfig-productionvariant-syntax.json"></a>

```
{
  "[ModelName](#cfn-sagemaker-endpointconfig-productionvariant-modelname)" : String,
  "[VariantName](#cfn-sagemaker-endpointconfig-productionvariant-variantname)" : String,
  "[InitialInstanceCount](#cfn-sagemaker-endpointconfig-productionvariant-initialinstancecount)" : Integer,
  "[InstanceType](#cfn-sagemaker-endpointconfig-productionvariant-instancetype)" : String,
  "[InitialVariantWeight](#cfn-sagemaker-endpointconfig-productionvariant-initialvariantweight)" : Double,
}
```

### YAML<a name="aws-properties-sagemaker-endpointconfig-productionvariant-syntax.yaml"></a>

```
[ModelName](#cfn-sagemaker-endpointconfig-productionvariant-modelname): String
[VariantName](#cfn-sagemaker-endpointconfig-productionvariant-variantname): String
[InitialInstanceCount](#cfn-sagemaker-endpointconfig-productionvariant-initialinstancecount): Integer
[InstanceType](#cfn-sagemaker-endpointconfig-productionvariant-instancetype): String
[InitialVariantWeight](#cfn-sagemaker-endpointconfig-productionvariant-initialvariantweight): Double
```

## Properties<a name="aws-properties-sagemaker-endpointconfig-productionvariant-properties"></a>

`ModelName`  <a name="cfn-sagemaker-endpointconfig-productionvariant-modelname"></a>
The name of the model that you want to host\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`VariantName`  <a name="cfn-sagemaker-endpointconfig-productionvariant-variantname"></a>
The name of the production variant\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`InitialInstanceCount`  <a name="cfn-sagemaker-endpointconfig-productionvariant-initialinstancecount"></a>
The number of instances to launch initially for this production variant\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`InstanceType`  <a name="cfn-sagemaker-endpointconfig-productionvariant-instancetype"></a>
The ML compute instance type to use for this production variant\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`InitialVariantWeight`  <a name="cfn-sagemaker-endpointconfig-productionvariant-initialvariantweight"></a>
Determines initial traffic distribution among all of the models that you specify in the endpoint configuration\. The traffic to a production variant is determined by the ratio of the `VariantWeight` to the sum of all `VariantWeight` values across all production variants for an endpoint\. If unspecified, it defaults to 1\.0\.   
 *Required*: Yes  
 *Type*: Double  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 