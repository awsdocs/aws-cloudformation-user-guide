# AWS::SageMaker::UserProfile TensorBoardAppSettings<a name="aws-properties-sagemaker-userprofile-tensorboardappsettings"></a>

The TensorBoard app settings\.

## Syntax<a name="aws-properties-sagemaker-userprofile-tensorboardappsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-userprofile-tensorboardappsettings-syntax.json"></a>

```
{
  "[DefaultResourceSpec](#cfn-sagemaker-userprofile-tensorboardappsettings-defaultresourcespec)" : ResourceSpec
}
```

### YAML<a name="aws-properties-sagemaker-userprofile-tensorboardappsettings-syntax.yaml"></a>

```
  [DefaultResourceSpec](#cfn-sagemaker-userprofile-tensorboardappsettings-defaultresourcespec): 
    ResourceSpec
```

## Properties<a name="aws-properties-sagemaker-userprofile-tensorboardappsettings-properties"></a>

`DefaultResourceSpec`  <a name="cfn-sagemaker-userprofile-tensorboardappsettings-defaultresourcespec"></a>
The default instance type and the Amazon Resource Name \(ARN\) of the SageMaker image created on the instance\.  
*Required*: No  
*Type*: [ResourceSpec](aws-properties-sagemaker-userprofile-resourcespec.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)