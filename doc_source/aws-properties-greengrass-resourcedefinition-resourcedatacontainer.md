# AWS IoT Greengrass ResourceDefinition ResourceDataContainer<a name="aws-properties-greengrass-resourcedefinition-resourcedatacontainer"></a>

<a name="aws-properties-greengrass-resourcedefinition-resourcedatacontainer-description"></a>A container for resource data, which defines the resource type\. The container takes only one of the following supported resource data types: `LocalDeviceResourceData`, `LocalVolumeResourceData`, `SageMakerMachineLearningModelResourceData`, `S3MachineLearningModelResourceData`, or `SecretsManagerSecretResourceData`\.

<a name="aws-properties-greengrass-resourcedefinition-resourcedatacontainer-inheritance"></a> In an AWS CloudFormation template, `ResourceDataContainer` is a property of the [ResourceInstance](aws-properties-greengrass-resourcedefinition-resourceinstance.md) property type\.

## Syntax<a name="aws-properties-greengrass-resourcedefinition-resourcedatacontainer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-resourcedefinition-resourcedatacontainer-syntax.json"></a>

**Note**  
Use only one of the following\.

```
{
  "[SecretsManagerSecretResourceData](#cfn-greengrass-resourcedefinition-resourcedatacontainer-secretsmanagersecretresourcedata)" : [*SecretsManagerSecretResourceData*](aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata.md),
  "[SageMakerMachineLearningModelResourceData](#cfn-greengrass-resourcedefinition-resourcedatacontainer-sagemakermachinelearningmodelresourcedata)" : [*SageMakerMachineLearningModelResourceData*](aws-properties-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata.md),
  "[LocalVolumeResourceData](#cfn-greengrass-resourcedefinition-resourcedatacontainer-localvolumeresourcedata)" : [*LocalVolumeResourceData*](aws-properties-greengrass-resourcedefinition-localvolumeresourcedata.md),
  "[LocalDeviceResourceData](#cfn-greengrass-resourcedefinition-resourcedatacontainer-localdeviceresourcedata)" : [*LocalDeviceResourceData*](aws-properties-greengrass-resourcedefinition-localdeviceresourcedata.md),
  "[S3MachineLearningModelResourceData](#cfn-greengrass-resourcedefinition-resourcedatacontainer-s3machinelearningmodelresourcedata)" : [*S3MachineLearningModelResourceData*](aws-properties-greengrass-resourcedefinition-s3machinelearningmodelresourcedata.md)
}
```

### YAML<a name="aws-properties-greengrass-resourcedefinition-resourcedatacontainer-syntax.yaml"></a>

**Note**  
Use only one of the following\.

```
[SecretsManagerSecretResourceData](#cfn-greengrass-resourcedefinition-resourcedatacontainer-secretsmanagersecretresourcedata): 
  [*SecretsManagerSecretResourceData*](aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata.md)
[SageMakerMachineLearningModelResourceData](#cfn-greengrass-resourcedefinition-resourcedatacontainer-sagemakermachinelearningmodelresourcedata): 
  [*SageMakerMachineLearningModelResourceData*](aws-properties-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata.md)
[LocalVolumeResourceData](#cfn-greengrass-resourcedefinition-resourcedatacontainer-localvolumeresourcedata): 
  [*LocalVolumeResourceData*](aws-properties-greengrass-resourcedefinition-localvolumeresourcedata.md)
[LocalDeviceResourceData](#cfn-greengrass-resourcedefinition-resourcedatacontainer-localdeviceresourcedata): 
  [*LocalDeviceResourceData*](aws-properties-greengrass-resourcedefinition-localdeviceresourcedata.md)
[S3MachineLearningModelResourceData](#cfn-greengrass-resourcedefinition-resourcedatacontainer-s3machinelearningmodelresourcedata): 
  [*S3MachineLearningModelResourceData*](aws-properties-greengrass-resourcedefinition-s3machinelearningmodelresourcedata.md)
```

## Properties<a name="aws-properties-greengrass-resourcedefinition-resourcedatacontainer-properties"></a>

`SecretsManagerSecretResourceData`  <a name="cfn-greengrass-resourcedefinition-resourcedatacontainer-secretsmanagersecretresourcedata"></a>
Settings for a secret resource\.  
 *Required*: No  
 *Type*: [SecretsManagerSecretResourceData](aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SageMakerMachineLearningModelResourceData`  <a name="cfn-greengrass-resourcedefinition-resourcedatacontainer-sagemakermachinelearningmodelresourcedata"></a>
Settings for a machine learning resource saved as an Amazon SageMaker training job\.  
 *Required*: No  
 *Type*: [SageMakerMachineLearningModelResourceData](aws-properties-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`LocalVolumeResourceData`  <a name="cfn-greengrass-resourcedefinition-resourcedatacontainer-localvolumeresourcedata"></a>
Settings for a local volume resource\.  
 *Required*: No  
 *Type*: [LocalVolumeResourceData](aws-properties-greengrass-resourcedefinition-localvolumeresourcedata.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`LocalDeviceResourceData`  <a name="cfn-greengrass-resourcedefinition-resourcedatacontainer-localdeviceresourcedata"></a>
Settings for a local device resource\.  
 *Required*: No  
 *Type*: [LocalDeviceResourceData](aws-properties-greengrass-resourcedefinition-localdeviceresourcedata.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`S3MachineLearningModelResourceData`  <a name="cfn-greengrass-resourcedefinition-resourcedatacontainer-s3machinelearningmodelresourcedata"></a>
Settings for a machine learning resource stored in Amazon S3\.  
 *Required*: No  
 *Type*: [S3MachineLearningModelResourceData](aws-properties-greengrass-resourcedefinition-s3machinelearningmodelresourcedata.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-resourcedefinition-resourcedatacontainer-seealso"></a>
+ [ResourceDataContainer](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-resourcedatacontainer.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)