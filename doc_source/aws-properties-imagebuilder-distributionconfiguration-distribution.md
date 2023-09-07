# AWS::ImageBuilder::DistributionConfiguration Distribution<a name="aws-properties-imagebuilder-distributionconfiguration-distribution"></a>

 The distribution configuration distribution defines the settings for a specific Region in the Distribution Configuration\. You must specify whether the distribution is for an AMI or a container image\. To do so, include exactly one of the following data types for your distribution:
+ amiDistributionConfiguration
+ containerDistributionConfiguration

## Syntax<a name="aws-properties-imagebuilder-distributionconfiguration-distribution-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-distributionconfiguration-distribution-syntax.json"></a>

```
{
  "[AmiDistributionConfiguration](#cfn-imagebuilder-distributionconfiguration-distribution-amidistributionconfiguration)" : AmiDistributionConfiguration,
  "[ContainerDistributionConfiguration](#cfn-imagebuilder-distributionconfiguration-distribution-containerdistributionconfiguration)" : ContainerDistributionConfiguration,
  "[FastLaunchConfigurations](#cfn-imagebuilder-distributionconfiguration-distribution-fastlaunchconfigurations)" : [ FastLaunchConfiguration, ... ],
  "[LaunchTemplateConfigurations](#cfn-imagebuilder-distributionconfiguration-distribution-launchtemplateconfigurations)" : [ LaunchTemplateConfiguration, ... ],
  "[LicenseConfigurationArns](#cfn-imagebuilder-distributionconfiguration-distribution-licenseconfigurationarns)" : [ String, ... ],
  "[Region](#cfn-imagebuilder-distributionconfiguration-distribution-region)" : String
}
```

### YAML<a name="aws-properties-imagebuilder-distributionconfiguration-distribution-syntax.yaml"></a>

```
  [AmiDistributionConfiguration](#cfn-imagebuilder-distributionconfiguration-distribution-amidistributionconfiguration): 
    AmiDistributionConfiguration
  [ContainerDistributionConfiguration](#cfn-imagebuilder-distributionconfiguration-distribution-containerdistributionconfiguration): 
    ContainerDistributionConfiguration
  [FastLaunchConfigurations](#cfn-imagebuilder-distributionconfiguration-distribution-fastlaunchconfigurations): 
    - FastLaunchConfiguration
  [LaunchTemplateConfigurations](#cfn-imagebuilder-distributionconfiguration-distribution-launchtemplateconfigurations): 
    - LaunchTemplateConfiguration
  [LicenseConfigurationArns](#cfn-imagebuilder-distributionconfiguration-distribution-licenseconfigurationarns): 
    - String
  [Region](#cfn-imagebuilder-distributionconfiguration-distribution-region): String
```

## Properties<a name="aws-properties-imagebuilder-distributionconfiguration-distribution-properties"></a>

`AmiDistributionConfiguration`  <a name="cfn-imagebuilder-distributionconfiguration-distribution-amidistributionconfiguration"></a>
 The specific AMI settings, such as launch permissions and AMI tags\. For details, see example schema below\.  
*Required*: No  
*Type*: [AmiDistributionConfiguration](aws-properties-imagebuilder-distributionconfiguration-amidistributionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContainerDistributionConfiguration`  <a name="cfn-imagebuilder-distributionconfiguration-distribution-containerdistributionconfiguration"></a>
Container distribution settings for encryption, licensing, and sharing in a specific Region\. For details, see example schema below\.  
*Required*: No  
*Type*: [ContainerDistributionConfiguration](aws-properties-imagebuilder-distributionconfiguration-containerdistributionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FastLaunchConfigurations`  <a name="cfn-imagebuilder-distributionconfiguration-distribution-fastlaunchconfigurations"></a>
The Windows faster\-launching configurations to use for AMI distribution\.  
*Required*: No  
*Type*: List of [FastLaunchConfiguration](aws-properties-imagebuilder-distributionconfiguration-fastlaunchconfiguration.md)  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplateConfigurations`  <a name="cfn-imagebuilder-distributionconfiguration-distribution-launchtemplateconfigurations"></a>
A group of launchTemplateConfiguration settings that apply to image distribution for specified accounts\.  
*Required*: No  
*Type*: List of [LaunchTemplateConfiguration](aws-properties-imagebuilder-distributionconfiguration-launchtemplateconfiguration.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LicenseConfigurationArns`  <a name="cfn-imagebuilder-distributionconfiguration-distribution-licenseconfigurationarns"></a>
 The License Manager Configuration to associate with the AMI in the specified Region\. For more information, see the [ LicenseConfiguration API](https://docs.aws.amazon.com/license-manager/latest/APIReference/API_LicenseConfiguration.html)\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-imagebuilder-distributionconfiguration-distribution-region"></a>
 The target Region for the Distribution Configuration\. For example, `eu-west-1`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-imagebuilder-distributionconfiguration-distribution--examples"></a>



### Example 1: AmiDistributionConfiguration schema with launch permissions<a name="aws-properties-imagebuilder-distributionconfiguration-distribution--examples--Example_1:_AmiDistributionConfiguration_schema_with_launch_permissions"></a>

The following example shows the schema for the AmiDistributionConfiguration property in both YAML and JSON format\.

**Note**  
To make an AMI public, set the launch permission authorized accounts to `all`\. See the examples for making an AMI public at [EC2 ModifyImageAttribute](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ModifyImageAttribute.html)\.

#### YAML<a name="aws-properties-imagebuilder-distributionconfiguration-distribution--examples--Example_1:_AmiDistributionConfiguration_schema_with_launch_permissions--yaml"></a>

```
Distributions:
  - Region: 'us-west-2'
    AmiDistributionConfiguration:
      Name: 'AmiCopyConfiguration - {{ imagebuilder:buildDate }}'
      Description: 'Share an AMI in the distribution Region by granting launch permissions to specified AWS organizations, OUs, user groups, and accounts.'
      AmiTags:
        AmiTagKey: 'AmiTagValue'
      LaunchPermissionConfiguration:
        OrganizationArns:
          - 'arn:aws:organizations::123456789012:organization/o-myorganization123'
        OrganizationalUnitArns:
          - 'arn:aws:organizations::123456789012:ou/o-123example/ou-1234-myorganizationalunit'
        UserGroups:
          - 'GroupName1'
          - 'GroupName2'
        UserIds:
          - '123456789012'
          - '345678901234'
```

#### JSON<a name="aws-properties-imagebuilder-distributionconfiguration-distribution--examples--Example_1:_AmiDistributionConfiguration_schema_with_launch_permissions--json"></a>

```
"{
    "Distributions": [{
        AmiDistributionConfiguration": {
        "Name": "AmiCopyConfiguration - {{ imagebuilder:buildDate }}",
        "Description": "Share an AMI in the distribution Region by granting launch permissions to specified user groups and accounts.",
        "AmiTags": {
            "AmiTagKey": "AmiTagValue"
        },
        "LaunchPermissionConfiguration": {
            "OrganizationArns": ["arn:aws:organizations::123456789012:organizatio ARNn/o-myorganization123"],
            "OrganizationalUnitArns": ["arn:aws:organizations::123456789012:ou/o-123example/ou-1234-myorganizationalunit"],
            "UserGroups": [
                "GroupName1",
                "GroupName2"
            ],
            "UserIds": [
                "123456789012",
                "345678901234"
            ]
        }
    }]
}
```

### Example 2: Create a distribution configuration resource for a copied AMI<a name="aws-properties-imagebuilder-distributionconfiguration-distribution--examples--Example_2:_Create_a_distribution_configuration_resource_for_a_copied_AMI"></a>

The following example shows the schema for the AmiDistributionConfiguration property in both YAML and JSON\.

#### YAML<a name="aws-properties-imagebuilder-distributionconfiguration-distribution--examples--Example_2:_Create_a_distribution_configuration_resource_for_a_copied_AMI--yaml"></a>

```
Distributions:
  - Region: 'us-west-2'
    AmiDistributionConfiguration:
      Name: AmiCopyConfiguration - {{ imagebuilder:buildDate }}
      Description: 'Distribute a copy of the AMI to specific accounts in the destination Region.'
      AmiTags:
        AmiTagKey: 'AmiTagValue'
      TargetAccountIds: 
        - '123456789012'
        - '345678901234'
```

#### JSON<a name="aws-properties-imagebuilder-distributionconfiguration-distribution--examples--Example_2:_Create_a_distribution_configuration_resource_for_a_copied_AMI--json"></a>

```
{
    "Distributions": [{
        "AmiDistributionConfiguration": {
            "Name": "AmiCopyConfiguration - {{ imagebuilder:buildDate }}",
            "Description": "Distribute a copy of the AMI to specific accounts in the destination Region.",
            "AmiTags": {
                "AmiTagKey": "AmiTagValue"
            },
            "TargetAccountIds": ["123456789012", "345678901234"]
        }
    }]
}
```

### Example 3: ContainerDistributionConfiguration schema<a name="aws-properties-imagebuilder-distributionconfiguration-distribution--examples--Example_3:_ContainerDistributionConfiguration_schema"></a>

The following example shows the schema for the ContainerDistributionConfiguration property in both YAML and JSON format\.

#### YAML<a name="aws-properties-imagebuilder-distributionconfiguration-distribution--examples--Example_3:_ContainerDistributionConfiguration_schema--yaml"></a>

```
Distributions:
  - Region: 'us-west-2'
    ContainerDistributionConfiguration:
      Description: 'test distribution cfn template'
      TargetRepository:
        Service: ECR
        RepositoryName: 'cfn-test'
      ContainerTags:
        - 'Tag1'
        - 'Tag2'
```

#### JSON<a name="aws-properties-imagebuilder-distributionconfiguration-distribution--examples--Example_3:_ContainerDistributionConfiguration_schema--json"></a>

```
{
    "Distributions": [{
        "ContainerDistributionConfiguration": {
            "Description": "test distribution cfn template",
            "TargetRepository": {
                "Service": "ECR",
                "RepositoryName": "cfn-test"
            },
            "ContainerTags": ["Tag1", "Tag2"]
        }
    }]
}
```