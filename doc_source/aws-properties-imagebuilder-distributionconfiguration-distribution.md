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
 The specific AMI settings, such as launch permissions and AMI tags\. For details, see example schema below\.  
*Required*: No  
*Type*: Json  
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



### Example AmiDistributionConfiguration schema<a name="aws-properties-imagebuilder-distributionconfiguration-distribution--examples--Example_AmiDistributionConfiguration_schema"></a>

The following example shows the schema for the AmiDistributionConfiguration property in both YAML and JSON format\. To make an AMI public, set the launch permission authorized accounts to `all`\. See the examples for making an AMI public at [EC2 ModifyImageAttribute](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ModifyImageAttribute.html)\. 

#### YAML<a name="aws-properties-imagebuilder-distributionconfiguration-distribution--examples--Example_AmiDistributionConfiguration_schema--yaml"></a>

```
AmiDistributionConfiguration:
  Name: 'AmiCopyConfiguration - {{ imagebuilder:buildDate }}'
  Description: 'description'
  AmiTags:
    AmiTagKey: 'AmiTagValue'
  LaunchPermissionConfiguration:
    UserGroups:
      - 'String - group name 1'
      - 'String - group name 1'
    UserIds:
      - 'String - account id 1'
      - 'String - account id 2'
```

#### JSON<a name="aws-properties-imagebuilder-distributionconfiguration-distribution--examples--Example_AmiDistributionConfiguration_schema--json"></a>

```
"AmiDistributionConfiguration": {
    "Name": "AmiCopyConfiguration - {{ imagebuilder:buildDate }}",
    "Description": "description",
    "AmiTags": {
        "AmiTagKey": "AmiTagValue"
    },
    "LaunchPermissionConfiguration": {
        "UserGroups": [
            "GroupName1",
            "GroupName2"
        ],
        "UserIds": [
            "123456789012",
            "345678901234"
        ]
    }
}
```