# AWS::SageMaker::AppImageConfig<a name="aws-resource-sagemaker-appimageconfig"></a>

Creates a configuration for running a SageMaker image as a KernelGateway app\. The configuration specifies the Amazon Elastic File System \(EFS\) storage volume on the image, and a list of the kernels in the image\.

## Syntax<a name="aws-resource-sagemaker-appimageconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-appimageconfig-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::AppImageConfig",
  "Properties" : {
      "[AppImageConfigName](#cfn-sagemaker-appimageconfig-appimageconfigname)" : String,
      "[KernelGatewayImageConfig](#cfn-sagemaker-appimageconfig-kernelgatewayimageconfig)" : KernelGatewayImageConfig,
      "[Tags](#cfn-sagemaker-appimageconfig-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-sagemaker-appimageconfig-syntax.yaml"></a>

```
Type: AWS::SageMaker::AppImageConfig
Properties: 
  [AppImageConfigName](#cfn-sagemaker-appimageconfig-appimageconfigname): String
  [KernelGatewayImageConfig](#cfn-sagemaker-appimageconfig-kernelgatewayimageconfig): 
    KernelGatewayImageConfig
  [Tags](#cfn-sagemaker-appimageconfig-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sagemaker-appimageconfig-properties"></a>

`AppImageConfigName`  <a name="cfn-sagemaker-appimageconfig-appimageconfigname"></a>
The name of the AppImageConfig\. Must be unique to your account\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KernelGatewayImageConfig`  <a name="cfn-sagemaker-appimageconfig-kernelgatewayimageconfig"></a>
The configuration for the file system and kernels in the SageMaker image\.  
*Required*: No  
*Type*: [KernelGatewayImageConfig](aws-properties-sagemaker-appimageconfig-kernelgatewayimageconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-sagemaker-appimageconfig-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sagemaker-appimageconfig-return-values"></a>

### Ref<a name="aws-resource-sagemaker-appimageconfig-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the AppImageConfig\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-sagemaker-appimageconfig-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-sagemaker-appimageconfig-return-values-fn--getatt-fn--getatt"></a>

`AppImageConfigArn`  <a name="AppImageConfigArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the AppImageConfig, such as `arn:aws:sagemaker:us-west-2:account-id:app-image-config/my-app-image-config-name`\.