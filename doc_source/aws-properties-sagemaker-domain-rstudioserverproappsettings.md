# AWS::SageMaker::Domain RStudioServerProAppSettings<a name="aws-properties-sagemaker-domain-rstudioserverproappsettings"></a>

A collection of settings that configure user interaction with the `RStudioServerPro` app\. `RStudioServerProAppSettings` cannot be updated\. The `RStudioServerPro` app must be deleted and a new one created to make any changes\.

## Syntax<a name="aws-properties-sagemaker-domain-rstudioserverproappsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-domain-rstudioserverproappsettings-syntax.json"></a>

```
{
  "[AccessStatus](#cfn-sagemaker-domain-rstudioserverproappsettings-accessstatus)" : String,
  "[UserGroup](#cfn-sagemaker-domain-rstudioserverproappsettings-usergroup)" : String
}
```

### YAML<a name="aws-properties-sagemaker-domain-rstudioserverproappsettings-syntax.yaml"></a>

```
  [AccessStatus](#cfn-sagemaker-domain-rstudioserverproappsettings-accessstatus): String
  [UserGroup](#cfn-sagemaker-domain-rstudioserverproappsettings-usergroup): String
```

## Properties<a name="aws-properties-sagemaker-domain-rstudioserverproappsettings-properties"></a>

`AccessStatus`  <a name="cfn-sagemaker-domain-rstudioserverproappsettings-accessstatus"></a>
Indicates whether the current user has access to the `RStudioServerPro` app\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserGroup`  <a name="cfn-sagemaker-domain-rstudioserverproappsettings-usergroup"></a>
The level of permissions that the user has within the `RStudioServerPro` app\. This value defaults to `User`\. The `Admin` value allows the user access to the RStudio Administrative Dashboard\.  
*Required*: No  
*Type*: String  
*Allowed values*: `R_STUDIO_ADMIN | R_STUDIO_USER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)