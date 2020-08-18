# AWS::Greengrass::ResourceDefinitionVersion S3MachineLearningModelResourceData<a name="aws-properties-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata"></a>

<a name="aws-properties-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-description"></a>Settings for an Amazon S3 machine learning resource\. For more information, see [Perform Machine Learning Inference](https://docs.aws.amazon.com/greengrass/latest/developerguide/ml-inference.html) in the *AWS IoT Greengrass Developer Guide*\.

<a name="aws-properties-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-inheritance"></a> In an AWS CloudFormation template, `S3MachineLearningModelResourceData` can be used in the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinitionversion-resourcedatacontainer.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinitionversion-resourcedatacontainer.html) property type\.

## Syntax<a name="aws-properties-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-syntax.json"></a>

```
{
  "[DestinationPath](#cfn-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-destinationpath)" : String,
  "[OwnerSetting](#cfn-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-ownersetting)" : ResourceDownloadOwnerSetting,
  "[S3Uri](#cfn-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-s3uri)" : String
}
```

### YAML<a name="aws-properties-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-syntax.yaml"></a>

```
  [DestinationPath](#cfn-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-destinationpath): String
  [OwnerSetting](#cfn-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-ownersetting): 
    ResourceDownloadOwnerSetting
  [S3Uri](#cfn-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-s3uri): String
```

## Properties<a name="aws-properties-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-properties"></a>

`DestinationPath`  <a name="cfn-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-destinationpath"></a>
The absolute local path of the resource inside the Lambda environment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OwnerSetting`  <a name="cfn-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-ownersetting"></a>
The owner setting for the downloaded machine learning resource\. For more information, see [Access Machine Learning Resources from Lambda Functions](https://docs.aws.amazon.com/greengrass/latest/developerguide/access-ml-resources.html) in the *AWS IoT Greengrass Developer Guide*\.  
*Required*: No  
*Type*: [ResourceDownloadOwnerSetting](aws-properties-greengrass-resourcedefinitionversion-resourcedownloadownersetting.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Uri`  <a name="cfn-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata-s3uri"></a>
The URI of the source model in an Amazon S3 bucket\. The model package must be in `tar.gz` or `.zip` format\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata--seealso"></a>
+  [S3MachineLearningModelResourceData](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-s3machinelearningmodelresourcedata.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 