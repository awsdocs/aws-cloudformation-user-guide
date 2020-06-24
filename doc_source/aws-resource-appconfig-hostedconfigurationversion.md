# AWS::AppConfig::HostedConfigurationVersion<a name="aws-resource-appconfig-hostedconfigurationversion"></a>

Not currently supported by AWS CloudFormation\.

## Syntax<a name="aws-resource-appconfig-hostedconfigurationversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appconfig-hostedconfigurationversion-syntax.json"></a>

```
{
  "Type" : "AWS::AppConfig::HostedConfigurationVersion",
  "Properties" : {
      "[ApplicationId](#cfn-appconfig-hostedconfigurationversion-applicationid)" : String,
      "[ConfigurationProfileId](#cfn-appconfig-hostedconfigurationversion-configurationprofileid)" : String,
      "[Content](#cfn-appconfig-hostedconfigurationversion-content)" : String,
      "[ContentType](#cfn-appconfig-hostedconfigurationversion-contenttype)" : String,
      "[Description](#cfn-appconfig-hostedconfigurationversion-description)" : String,
      "[LatestVersionNumber](#cfn-appconfig-hostedconfigurationversion-latestversionnumber)" : Double
    }
}
```

### YAML<a name="aws-resource-appconfig-hostedconfigurationversion-syntax.yaml"></a>

```
Type: AWS::AppConfig::HostedConfigurationVersion
Properties: 
  [ApplicationId](#cfn-appconfig-hostedconfigurationversion-applicationid): String
  [ConfigurationProfileId](#cfn-appconfig-hostedconfigurationversion-configurationprofileid): String
  [Content](#cfn-appconfig-hostedconfigurationversion-content): String
  [ContentType](#cfn-appconfig-hostedconfigurationversion-contenttype): String
  [Description](#cfn-appconfig-hostedconfigurationversion-description): String
  [LatestVersionNumber](#cfn-appconfig-hostedconfigurationversion-latestversionnumber): Double
```

## Properties<a name="aws-resource-appconfig-hostedconfigurationversion-properties"></a>

`ApplicationId`  <a name="cfn-appconfig-hostedconfigurationversion-applicationid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-z0-9]{4,7}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationProfileId`  <a name="cfn-appconfig-hostedconfigurationversion-configurationprofileid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-z0-9]{4,7}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Content`  <a name="cfn-appconfig-hostedconfigurationversion-content"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContentType`  <a name="cfn-appconfig-hostedconfigurationversion-contenttype"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-appconfig-hostedconfigurationversion-description"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LatestVersionNumber`  <a name="cfn-appconfig-hostedconfigurationversion-latestversionnumber"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)