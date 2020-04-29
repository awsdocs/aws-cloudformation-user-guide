# AWS::ImageBuilder::DistributionConfiguration Distribution<a name="aws-properties-imagebuilder-distributionconfiguration-distribution"></a>

 The distribution configuration distribution defines the settings for a specific Region in the Distribution Configuration\. 

## Syntax<a name="aws-properties-imagebuilder-distributionconfiguration-distribution-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-distributionconfiguration-distribution-syntax.json"></a>

```
{
  "[AmiDistributionConfiguration](#cfn-imagebuilder-distributionconfiguration-distribution-amidistributionconfiguration)" : Json,
  "[LicenseConfigurationArns](#cfn-imagebuilder-distributionconfiguration-distribution-licenseconfigurationarns)" : [ String, ... ],
  "[Region](#cfn-imagebuilder-distributionconfiguration-distribution-region)" : String
}
```

### YAML<a name="aws-properties-imagebuilder-distributionconfiguration-distribution-syntax.yaml"></a>

```
  [AmiDistributionConfiguration](#cfn-imagebuilder-distributionconfiguration-distribution-amidistributionconfiguration): Json
  [LicenseConfigurationArns](#cfn-imagebuilder-distributionconfiguration-distribution-licenseconfigurationarns): 
    - String
  [Region](#cfn-imagebuilder-distributionconfiguration-distribution-region): String
```

## Properties<a name="aws-properties-imagebuilder-distributionconfiguration-distribution-properties"></a>

`AmiDistributionConfiguration`  <a name="cfn-imagebuilder-distributionconfiguration-distribution-amidistributionconfiguration"></a>
 The specific AMI settings, such as launch permissions and AMI tags\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LicenseConfigurationArns`  <a name="cfn-imagebuilder-distributionconfiguration-distribution-licenseconfigurationarns"></a>
 The License Manager Configuration to associate with the AMI in the specified Region\. For more information, see the [ LicenseConfiguration API](https://docs.aws.amazon.com/license-manager/latest/APIReference/API_LicenseConfiguration.html)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-imagebuilder-distributionconfiguration-distribution-region"></a>
 The target Region for the Distribution Configuration\. For example, `eu-west-1`\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)