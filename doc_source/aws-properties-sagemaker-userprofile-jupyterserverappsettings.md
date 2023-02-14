# AWS::SageMaker::UserProfile JupyterServerAppSettings<a name="aws-properties-sagemaker-userprofile-jupyterserverappsettings"></a>

The JupyterServer app settings\.

## Syntax<a name="aws-properties-sagemaker-userprofile-jupyterserverappsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-userprofile-jupyterserverappsettings-syntax.json"></a>

```
{
  "[DefaultResourceSpec](#cfn-sagemaker-userprofile-jupyterserverappsettings-defaultresourcespec)" : ResourceSpec
}
```

### YAML<a name="aws-properties-sagemaker-userprofile-jupyterserverappsettings-syntax.yaml"></a>

```
  [DefaultResourceSpec](#cfn-sagemaker-userprofile-jupyterserverappsettings-defaultresourcespec): 
    ResourceSpec
```

## Properties<a name="aws-properties-sagemaker-userprofile-jupyterserverappsettings-properties"></a>

`DefaultResourceSpec`  <a name="cfn-sagemaker-userprofile-jupyterserverappsettings-defaultresourcespec"></a>
The default instance type and the Amazon Resource Name \(ARN\) of the default SageMaker image used by the JupyterServer app\.  
*Required*: No  
*Type*: [ResourceSpec](aws-properties-sagemaker-userprofile-resourcespec.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)