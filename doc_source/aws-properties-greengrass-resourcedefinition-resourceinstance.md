# AWS::Greengrass::ResourceDefinition ResourceInstance<a name="aws-properties-greengrass-resourcedefinition-resourceinstance"></a>

<a name="aws-properties-greengrass-resourcedefinition-resourceinstance-description"></a>A local resource, machine learning resource, or secret resource\. For more information, see [Access Local Resources with Lambda Functions](https://docs.aws.amazon.com/greengrass/latest/developerguide/access-local-resources.html), [Perform Machine Learning Inference](https://docs.aws.amazon.com/greengrass/latest/developerguide/ml-inference.html), and [Deploy Secrets to the AWS IoT Greengrass Core](https://docs.aws.amazon.com/greengrass/latest/developerguide/secrets.html) in the *AWS IoT Greengrass Developer Guide*\.

<a name="aws-properties-greengrass-resourcedefinition-resourceinstance-inheritance"></a> In an AWS CloudFormation template, the `Resources` property of the [ `AWS::Greengrass::ResourceDefinition` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinition.html) resource contains a list of `ResourceInstance` property types\.

## Syntax<a name="aws-properties-greengrass-resourcedefinition-resourceinstance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-resourcedefinition-resourceinstance-syntax.json"></a>

```
{
  "[Id](#cfn-greengrass-resourcedefinition-resourceinstance-id)" : String,
  "[Name](#cfn-greengrass-resourcedefinition-resourceinstance-name)" : String,
  "[ResourceDataContainer](#cfn-greengrass-resourcedefinition-resourceinstance-resourcedatacontainer)" : ResourceDataContainer
}
```

### YAML<a name="aws-properties-greengrass-resourcedefinition-resourceinstance-syntax.yaml"></a>

```
  [Id](#cfn-greengrass-resourcedefinition-resourceinstance-id): String
  [Name](#cfn-greengrass-resourcedefinition-resourceinstance-name): String
  [ResourceDataContainer](#cfn-greengrass-resourcedefinition-resourceinstance-resourcedatacontainer): 
    ResourceDataContainer
```

## Properties<a name="aws-properties-greengrass-resourcedefinition-resourceinstance-properties"></a>

`Id`  <a name="cfn-greengrass-resourcedefinition-resourceinstance-id"></a>
A descriptive or arbitrary ID for the resource\. This value must be unique within the resource definition version\. Maximum length is 128 characters with pattern `[a-zA-Z0-9:_-]+`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-greengrass-resourcedefinition-resourceinstance-name"></a>
The descriptive resource name, which is displayed on the AWS IoT Greengrass console\. Maximum length 128 characters with pattern \[a\-zA\-Z0\-9:\_\-\]\+\. This must be unique within a Greengrass group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceDataContainer`  <a name="cfn-greengrass-resourcedefinition-resourceinstance-resourcedatacontainer"></a>
A container for resource data\. The container takes only one of the following supported resource data types: `LocalDeviceResourceData`, `LocalVolumeResourceData`, `SageMakerMachineLearningModelResourceData`, `S3MachineLearningModelResourceData`, or `SecretsManagerSecretResourceData`\.  
Only one resource type can be defined for a `ResourceDataContainer` instance\.
*Required*: Yes  
*Type*: [ResourceDataContainer](aws-properties-greengrass-resourcedefinition-resourcedatacontainer.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-resourcedefinition-resourceinstance--seealso"></a>
+  [Resource](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-resource.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 