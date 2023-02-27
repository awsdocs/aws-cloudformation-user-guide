# AWS::SageMaker::Domain RStudioServerProDomainSettings<a name="aws-properties-sagemaker-domain-rstudioserverprodomainsettings"></a>

A collection of settings that configure the `RStudioServerPro` Domain\-level app\.

## Syntax<a name="aws-properties-sagemaker-domain-rstudioserverprodomainsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-domain-rstudioserverprodomainsettings-syntax.json"></a>

```
{
  "[DefaultResourceSpec](#cfn-sagemaker-domain-rstudioserverprodomainsettings-defaultresourcespec)" : ResourceSpec,
  "[DomainExecutionRoleArn](#cfn-sagemaker-domain-rstudioserverprodomainsettings-domainexecutionrolearn)" : String,
  "[RStudioConnectUrl](#cfn-sagemaker-domain-rstudioserverprodomainsettings-rstudioconnecturl)" : String,
  "[RStudioPackageManagerUrl](#cfn-sagemaker-domain-rstudioserverprodomainsettings-rstudiopackagemanagerurl)" : String
}
```

### YAML<a name="aws-properties-sagemaker-domain-rstudioserverprodomainsettings-syntax.yaml"></a>

```
  [DefaultResourceSpec](#cfn-sagemaker-domain-rstudioserverprodomainsettings-defaultresourcespec): 
    ResourceSpec
  [DomainExecutionRoleArn](#cfn-sagemaker-domain-rstudioserverprodomainsettings-domainexecutionrolearn): String
  [RStudioConnectUrl](#cfn-sagemaker-domain-rstudioserverprodomainsettings-rstudioconnecturl): String
  [RStudioPackageManagerUrl](#cfn-sagemaker-domain-rstudioserverprodomainsettings-rstudiopackagemanagerurl): String
```

## Properties<a name="aws-properties-sagemaker-domain-rstudioserverprodomainsettings-properties"></a>

`DefaultResourceSpec`  <a name="cfn-sagemaker-domain-rstudioserverprodomainsettings-defaultresourcespec"></a>
A collection that defines the default `InstanceType`, `SageMakerImageArn`, and `SageMakerImageVersionArn` for the Domain\.  
*Required*: No  
*Type*: [ResourceSpec](aws-properties-sagemaker-domain-resourcespec.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DomainExecutionRoleArn`  <a name="cfn-sagemaker-domain-rstudioserverprodomainsettings-domainexecutionrolearn"></a>
The ARN of the execution role for the `RStudioServerPro` Domain\-level app\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RStudioConnectUrl`  <a name="cfn-sagemaker-domain-rstudioserverprodomainsettings-rstudioconnecturl"></a>
A URL pointing to an RStudio Connect server\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RStudioPackageManagerUrl`  <a name="cfn-sagemaker-domain-rstudioserverprodomainsettings-rstudiopackagemanagerurl"></a>
A URL pointing to an RStudio Package Manager server\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)