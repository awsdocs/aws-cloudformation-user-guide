# AWS IoT Greengrass ResourceDefinition SageMakerMachineLearningModelResourceData<a name="aws-properties-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata"></a>

<a name="aws-properties-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata-description"></a>Settings for an Secrets Manager machine learning resource\. For more information, see [Perform Machine Learning Inference](https://docs.aws.amazon.com/greengrass/latest/developerguide/ml-inference.html) in the *AWS IoT Greengrass Developer Guide*\.

<a name="aws-properties-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata-inheritance"></a> In an AWS CloudFormation template, `SageMakerMachineLearningModelResourceData` can be used in the [ResourceDataContainer](aws-properties-greengrass-resourcedefinition-resourcedatacontainer.md) property type\.

## Syntax<a name="aws-properties-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata-syntax.json"></a>

```
{
  "[DestinationPath](#cfn-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata-destinationpath)" : String,
  "[SageMakerJobArn](#cfn-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata-sagemakerjobarn)" : String
}
```

### YAML<a name="aws-properties-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata-syntax.yaml"></a>

```
[DestinationPath](#cfn-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata-destinationpath): String
[SageMakerJobArn](#cfn-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata-sagemakerjobarn): String
```

## Properties<a name="aws-properties-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata-properties"></a>

`DestinationPath`  <a name="cfn-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata-destinationpath"></a>
The absolute local path of the resource in the Lambda environment\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SageMakerJobArn`  <a name="cfn-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata-sagemakerjobarn"></a>
The Amazon Resource Name \(ARN\) of the Secrets Manager training job that represents the source model\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata-seealso"></a>
+ [SageMakerMachineLearningModelResourceData](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-sagemakermachinelearningmodelresourcedata.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)