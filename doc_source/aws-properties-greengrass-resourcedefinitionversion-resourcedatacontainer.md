# AWS IoT Greengrass ResourceDefinitionVersion ResourceDataContainer<a name="aws-properties-greengrass-resourcedefinitionversion-resourcedatacontainer"></a>

<a name="aws-properties-greengrass-resourcedefinitionversion-resourcedatacontainer-description"></a>A container for resource data, which defines the resource type\. The container takes only one of the following supported resource data types: `LocalDeviceResourceData`, `LocalVolumeResourceData`, `SageMakerMachineLearningModelResourceData`, `S3MachineLearningModelResourceData`, or `SecretsManagerSecretResourceData`\.

<a name="aws-properties-greengrass-resourcedefinitionversion-resourcedatacontainer-inheritance"></a> In an AWS CloudFormation template, `ResourceDataContainer` is a property of the [ResourceInstance](aws-properties-greengrass-resourcedefinitionversion-resourceinstance.md) property type\.

## Syntax<a name="aws-properties-greengrass-resourcedefinitionversion-resourcedatacontainer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-resourcedefinitionversion-resourcedatacontainer-syntax.json"></a>

**Note**  
Use only one of the following\.

```
{
  "[SecretsManagerSecretResourceData](#cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-secretsmanagersecretresourcedata)" : [*SecretsManagerSecretResourceData*](aws-properties-greengrass-resourcedefinitionversion-secretsmanagersecretresourcedata.md),
  "[SageMakerMachineLearningModelResourceData](#cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-sagemakermachinelearningmodelresourcedata)" : [*SageMakerMachineLearningModelResourceData*](aws-properties-greengrass-resourcedefinitionversion-sagemakermachinelearningmodelresourcedata.md),
  "[LocalVolumeResourceData](#cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-localvolumeresourcedata)" : [*LocalVolumeResourceData*](aws-properties-greengrass-resourcedefinitionversion-localvolumeresourcedata.md),
  "[LocalDeviceResourceData](#cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-localdeviceresourcedata)" : [*LocalDeviceResourceData*](aws-properties-greengrass-resourcedefinitionversion-localdeviceresourcedata.md),
  "[S3MachineLearningModelResourceData](#cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-s3machinelearningmodelresourcedata)" : [*S3MachineLearningModelResourceData*](aws-properties-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata.md)
}
```

### YAML<a name="aws-properties-greengrass-resourcedefinitionversion-resourcedatacontainer-syntax.yaml"></a>

**Note**  
Use only one of the following\.

```
[SecretsManagerSecretResourceData](#cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-secretsmanagersecretresourcedata): 
  [*SecretsManagerSecretResourceData*](aws-properties-greengrass-resourcedefinitionversion-secretsmanagersecretresourcedata.md)
[SageMakerMachineLearningModelResourceData](#cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-sagemakermachinelearningmodelresourcedata): 
  [*SageMakerMachineLearningModelResourceData*](aws-properties-greengrass-resourcedefinitionversion-sagemakermachinelearningmodelresourcedata.md)
[LocalVolumeResourceData](#cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-localvolumeresourcedata): 
  [*LocalVolumeResourceData*](aws-properties-greengrass-resourcedefinitionversion-localvolumeresourcedata.md)
[LocalDeviceResourceData](#cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-localdeviceresourcedata): 
  [*LocalDeviceResourceData*](aws-properties-greengrass-resourcedefinitionversion-localdeviceresourcedata.md)
[S3MachineLearningModelResourceData](#cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-s3machinelearningmodelresourcedata): 
  [*S3MachineLearningModelResourceData*](aws-properties-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata.md)
```

## Properties<a name="aws-properties-greengrass-resourcedefinitionversion-resourcedatacontainer-properties"></a>

`SecretsManagerSecretResourceData`  <a name="cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-secretsmanagersecretresourcedata"></a>
Settings for a secret resource\.  
 *Required*: No  
 *Type*: [SecretsManagerSecretResourceData](aws-properties-greengrass-resourcedefinitionversion-secretsmanagersecretresourcedata.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SageMakerMachineLearningModelResourceData`  <a name="cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-sagemakermachinelearningmodelresourcedata"></a>
Settings for a machine learning resource saved as an Amazon SageMaker training job\.  
 *Required*: No  
 *Type*: [SageMakerMachineLearningModelResourceData](aws-properties-greengrass-resourcedefinitionversion-sagemakermachinelearningmodelresourcedata.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`LocalVolumeResourceData`  <a name="cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-localvolumeresourcedata"></a>
Settings for a local volume resource\.  
 *Required*: No  
 *Type*: [LocalVolumeResourceData](aws-properties-greengrass-resourcedefinitionversion-localvolumeresourcedata.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`LocalDeviceResourceData`  <a name="cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-localdeviceresourcedata"></a>
Settings for a local device resource\.  
 *Required*: No  
 *Type*: [LocalDeviceResourceData](aws-properties-greengrass-resourcedefinitionversion-localdeviceresourcedata.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`S3MachineLearningModelResourceData`  <a name="cfn-greengrass-resourcedefinitionversion-resourcedatacontainer-s3machinelearningmodelresourcedata"></a>
Settings for a machine learning resource stored in Amazon S3\.  
 *Required*: No  
 *Type*: [S3MachineLearningModelResourceData](aws-properties-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-resourcedefinitionversion-resourcedatacontainer-seealso"></a>
+ [ResourceDataContainer](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-resourcedatacontainer.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)