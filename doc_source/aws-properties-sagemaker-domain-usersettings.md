# AWS::SageMaker::Domain UserSettings<a name="aws-properties-sagemaker-domain-usersettings"></a>

A collection of settings that apply to users of Amazon SageMaker Studio\. These settings are specified when the [CreateUserProfile](https://docs.aws.amazon.com/sagemaker/latest/APIReference/API_CreateUserProfile.html) API is called, and as `DefaultUserSettings` when the [CreateDomain](https://docs.aws.amazon.com/sagemaker/latest/APIReference/API_CreateDomain.html) API is called\.

 `SecurityGroups` is aggregated when specified in both calls\. For all other settings in `UserSettings`, the values specified in `CreateUserProfile` take precedence over those specified in `CreateDomain`\.

## Syntax<a name="aws-properties-sagemaker-domain-usersettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-domain-usersettings-syntax.json"></a>

```
{
  "[ExecutionRole](#cfn-sagemaker-domain-usersettings-executionrole)" : String,
  "[JupyterServerAppSettings](#cfn-sagemaker-domain-usersettings-jupyterserverappsettings)" : JupyterServerAppSettings,
  "[KernelGatewayAppSettings](#cfn-sagemaker-domain-usersettings-kernelgatewayappsettings)" : KernelGatewayAppSettings,
  "[RSessionAppSettings](#cfn-sagemaker-domain-usersettings-rsessionappsettings)" : RSessionAppSettings,
  "[RStudioServerProAppSettings](#cfn-sagemaker-domain-usersettings-rstudioserverproappsettings)" : RStudioServerProAppSettings,
  "[SecurityGroups](#cfn-sagemaker-domain-usersettings-securitygroups)" : [ String, ... ],
  "[SharingSettings](#cfn-sagemaker-domain-usersettings-sharingsettings)" : SharingSettings
}
```

### YAML<a name="aws-properties-sagemaker-domain-usersettings-syntax.yaml"></a>

```
  [ExecutionRole](#cfn-sagemaker-domain-usersettings-executionrole): String
  [JupyterServerAppSettings](#cfn-sagemaker-domain-usersettings-jupyterserverappsettings): 
    JupyterServerAppSettings
  [KernelGatewayAppSettings](#cfn-sagemaker-domain-usersettings-kernelgatewayappsettings): 
    KernelGatewayAppSettings
  [RSessionAppSettings](#cfn-sagemaker-domain-usersettings-rsessionappsettings): 
    RSessionAppSettings
  [RStudioServerProAppSettings](#cfn-sagemaker-domain-usersettings-rstudioserverproappsettings): 
    RStudioServerProAppSettings
  [SecurityGroups](#cfn-sagemaker-domain-usersettings-securitygroups): 
    - String
  [SharingSettings](#cfn-sagemaker-domain-usersettings-sharingsettings): 
    SharingSettings
```

## Properties<a name="aws-properties-sagemaker-domain-usersettings-properties"></a>

`ExecutionRole`  <a name="cfn-sagemaker-domain-usersettings-executionrole"></a>
The execution role for the user\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JupyterServerAppSettings`  <a name="cfn-sagemaker-domain-usersettings-jupyterserverappsettings"></a>
The Jupyter server's app settings\.  
*Required*: No  
*Type*: [JupyterServerAppSettings](aws-properties-sagemaker-domain-jupyterserverappsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KernelGatewayAppSettings`  <a name="cfn-sagemaker-domain-usersettings-kernelgatewayappsettings"></a>
The kernel gateway app settings\.  
*Required*: No  
*Type*: [KernelGatewayAppSettings](aws-properties-sagemaker-domain-kernelgatewayappsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RSessionAppSettings`  <a name="cfn-sagemaker-domain-usersettings-rsessionappsettings"></a>
A collection of settings that configure the `RSessionGateway` app\.  
*Required*: No  
*Type*: [RSessionAppSettings](aws-properties-sagemaker-domain-rsessionappsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RStudioServerProAppSettings`  <a name="cfn-sagemaker-domain-usersettings-rstudioserverproappsettings"></a>
A collection of settings that configure user interaction with the `RStudioServerPro` app\.  
*Required*: No  
*Type*: [RStudioServerProAppSettings](aws-properties-sagemaker-domain-rstudioserverproappsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroups`  <a name="cfn-sagemaker-domain-usersettings-securitygroups"></a>
The security groups for the Amazon Virtual Private Cloud \(VPC\) that Studio uses for communication\.  
Optional when the `CreateDomain.AppNetworkAccessType` parameter is set to `PublicInternetOnly`\.  
Required when the `CreateDomain.AppNetworkAccessType` parameter is set to `VpcOnly`\.  
Amazon SageMaker adds a security group to allow NFS traffic from SageMaker Studio\. Therefore, the number of security groups that you can specify is one less than the maximum number shown\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SharingSettings`  <a name="cfn-sagemaker-domain-usersettings-sharingsettings"></a>
Specifies options for sharing SageMaker Studio notebooks\.  
*Required*: No  
*Type*: [SharingSettings](aws-properties-sagemaker-domain-sharingsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)