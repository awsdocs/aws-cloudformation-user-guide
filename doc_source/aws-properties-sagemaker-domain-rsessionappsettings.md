# AWS::SageMaker::Domain RSessionAppSettings<a name="aws-properties-sagemaker-domain-rsessionappsettings"></a>

A collection of settings that apply to an `RSessionGateway` app\.

## Syntax<a name="aws-properties-sagemaker-domain-rsessionappsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-domain-rsessionappsettings-syntax.json"></a>

```
{
  "[CustomImages](#cfn-sagemaker-domain-rsessionappsettings-customimages)" : [ CustomImage, ... ],
  "[DefaultResourceSpec](#cfn-sagemaker-domain-rsessionappsettings-defaultresourcespec)" : ResourceSpec
}
```

### YAML<a name="aws-properties-sagemaker-domain-rsessionappsettings-syntax.yaml"></a>

```
  [CustomImages](#cfn-sagemaker-domain-rsessionappsettings-customimages): 
    - CustomImage
  [DefaultResourceSpec](#cfn-sagemaker-domain-rsessionappsettings-defaultresourcespec): 
    ResourceSpec
```

## Properties<a name="aws-properties-sagemaker-domain-rsessionappsettings-properties"></a>

`CustomImages`  <a name="cfn-sagemaker-domain-rsessionappsettings-customimages"></a>
A list of custom SageMaker images that are configured to run as a RSession app\.  
*Required*: No  
*Type*: List of [CustomImage](aws-properties-sagemaker-domain-customimage.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultResourceSpec`  <a name="cfn-sagemaker-domain-rsessionappsettings-defaultresourcespec"></a>
Specifies the ARNs of a SageMaker image and SageMaker image version, and the instance type that the version runs on\.  
*Required*: No  
*Type*: [ResourceSpec](aws-properties-sagemaker-domain-resourcespec.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)