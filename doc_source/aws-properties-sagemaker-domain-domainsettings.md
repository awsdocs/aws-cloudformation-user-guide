# AWS::SageMaker::Domain DomainSettings<a name="aws-properties-sagemaker-domain-domainsettings"></a>

A collection of settings that apply to the `SageMaker Domain`\. These settings are specified through the `CreateDomain` API call\.

## Syntax<a name="aws-properties-sagemaker-domain-domainsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-domain-domainsettings-syntax.json"></a>

```
{
  "[RStudioServerProDomainSettings](#cfn-sagemaker-domain-domainsettings-rstudioserverprodomainsettings)" : RStudioServerProDomainSettings,
  "[SecurityGroupIds](#cfn-sagemaker-domain-domainsettings-securitygroupids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-domain-domainsettings-syntax.yaml"></a>

```
  [RStudioServerProDomainSettings](#cfn-sagemaker-domain-domainsettings-rstudioserverprodomainsettings): 
    RStudioServerProDomainSettings
  [SecurityGroupIds](#cfn-sagemaker-domain-domainsettings-securitygroupids): 
    - String
```

## Properties<a name="aws-properties-sagemaker-domain-domainsettings-properties"></a>

`RStudioServerProDomainSettings`  <a name="cfn-sagemaker-domain-domainsettings-rstudioserverprodomainsettings"></a>
A collection of settings that configure the `RStudioServerPro` Domain\-level app\.  
*Required*: No  
*Type*: [RStudioServerProDomainSettings](aws-properties-sagemaker-domain-rstudioserverprodomainsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-sagemaker-domain-domainsettings-securitygroupids"></a>
The security groups for the Amazon Virtual Private Cloud that the `Domain` uses for communication between Domain\-level apps and user apps\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)