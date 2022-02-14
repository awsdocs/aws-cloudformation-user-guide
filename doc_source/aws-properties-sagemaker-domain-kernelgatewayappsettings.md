# AWS::SageMaker::Domain KernelGatewayAppSettings<a name="aws-properties-sagemaker-domain-kernelgatewayappsettings"></a>

The KernelGateway app settings\.

## Syntax<a name="aws-properties-sagemaker-domain-kernelgatewayappsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-domain-kernelgatewayappsettings-syntax.json"></a>

```
{
  "[CustomImages](#cfn-sagemaker-domain-kernelgatewayappsettings-customimages)" : [ CustomImage, ... ],
  "[DefaultResourceSpec](#cfn-sagemaker-domain-kernelgatewayappsettings-defaultresourcespec)" : ResourceSpec
}
```

### YAML<a name="aws-properties-sagemaker-domain-kernelgatewayappsettings-syntax.yaml"></a>

```
  [CustomImages](#cfn-sagemaker-domain-kernelgatewayappsettings-customimages): 
    - CustomImage
  [DefaultResourceSpec](#cfn-sagemaker-domain-kernelgatewayappsettings-defaultresourcespec): 
    ResourceSpec
```

## Properties<a name="aws-properties-sagemaker-domain-kernelgatewayappsettings-properties"></a>

`CustomImages`  <a name="cfn-sagemaker-domain-kernelgatewayappsettings-customimages"></a>
A list of custom SageMaker images that are configured to run as a KernelGateway app\.  
*Required*: No  
*Type*: List of [CustomImage](aws-properties-sagemaker-domain-customimage.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultResourceSpec`  <a name="cfn-sagemaker-domain-kernelgatewayappsettings-defaultresourcespec"></a>
The default instance type and the Amazon Resource Name \(ARN\) of the default SageMaker image used by the KernelGateway app\.  
The Amazon SageMaker Studio UI does not use the default instance type value set here\. The default instance type set here is used when Apps are created using the AWS Command Line Interface or AWS CloudFormation and the instance type parameter value is not passed\.
*Required*: No  
*Type*: [ResourceSpec](aws-properties-sagemaker-domain-resourcespec.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)