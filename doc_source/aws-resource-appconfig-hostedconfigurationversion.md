# AWS::AppConfig::HostedConfigurationVersion<a name="aws-resource-appconfig-hostedconfigurationversion"></a>

Create a new configuration in the AppConfig hosted configuration store\. Configurations must be 64 KB or smaller\. The AppConfig hosted configuration store provides the following benefits over other configuration store options\.
+ You don't need to set up and configure other services such as Amazon Simple Storage Service \(Amazon S3\) or Parameter Store\.
+ You don't need to configure AWS Identity and Access Management \(IAM\) permissions to use the configuration store\.
+ You can store configurations in any content type\.
+ There is no cost to use the store\.
+ You can create a configuration and add it to the store when you create a configuration profile\.

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
The application ID\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-z0-9]{4,7}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationProfileId`  <a name="cfn-appconfig-hostedconfigurationversion-configurationprofileid"></a>
The configuration profile ID\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-z0-9]{4,7}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Content`  <a name="cfn-appconfig-hostedconfigurationversion-content"></a>
The content of the configuration or the configuration data\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContentType`  <a name="cfn-appconfig-hostedconfigurationversion-contenttype"></a>
A standard MIME type describing the format of the configuration content\. For more information, see [Content\-Type](https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.17)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-appconfig-hostedconfigurationversion-description"></a>
A description of the configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LatestVersionNumber`  <a name="cfn-appconfig-hostedconfigurationversion-latestversionnumber"></a>
An optional locking token used to prevent race conditions from overwriting configuration updates when creating a new version\. To ensure your data is not overwritten when creating multiple hosted configuration versions in rapid succession, specify the version number of the latest hosted configuration version\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-appconfig-hostedconfigurationversion-return-values"></a>

### Ref<a name="aws-resource-appconfig-hostedconfigurationversion-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the version number\.

## Examples<a name="aws-resource-appconfig-hostedconfigurationversion--examples"></a>



### AWS AppConfig hosted configuration<a name="aws-resource-appconfig-hostedconfigurationversion--examples--AWS_AppConfig_hosted_configuration"></a>

The following example creates an AWS AppConfig configuration profile named `MyTestProfile` for an application called `MyApplication`\. AppConfig stores the configuration data for this profile in the AppConfig hosted configuration store\.

#### JSON<a name="aws-resource-appconfig-hostedconfigurationversion--examples--AWS_AppConfig_hosted_configuration--json"></a>

```
{
  "Resources": {
    "DependentApplication": {
      "Type": "AWS::AppConfig::Application",
      "Properties": {
        "Name": "MyApplication"
      }
    },
    "DependentConfigurationProfile": {
      "Type": "AWS::AppConfig::ConfigurationProfile",
      "Properties": {
        "ApplicationId": "DependentApplication",
        "Name": "MyTestProfile",
        "LocationUri": "hosted"
      }
    },
    "BasicHostedConfigurationVersion": {
      "Type": "AWS::AppConfig::HostedConfigurationVersion",
      "Properties": {
        "ApplicationId": "DependentApplication",
        "ConfigurationProfileId": "DependentConfigurationProfile",
        "Description": "A sample hosted configuration version",
        "Content": "My hosted configuration content",
        "ContentType": "text/plain"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-appconfig-hostedconfigurationversion--examples--AWS_AppConfig_hosted_configuration--yaml"></a>

```
Resources:
  DependentApplication:
    Type: AWS::AppConfig::Application
    Properties:
      Name: "MyApplication"
  DependentConfigurationProfile:
    Type: AWS::AppConfig::ConfigurationProfile
    Properties:
      ApplicationId: !Ref DependentApplication
      Name: "MyTestProfile"
      LocationUri: "hosted"
  BasicHostedConfigurationVersion:
    Type: AWS::AppConfig::HostedConfigurationVersion
    Properties:
      ApplicationId: !Ref DependentApplication
      ConfigurationProfileId: !Ref DependentConfigurationProfile
      Description: 'A sample hosted configuration version'
      Content: 'My hosted configuration content'
      ContentType: 'text/plain'
```

## See also<a name="aws-resource-appconfig-hostedconfigurationversion--seealso"></a>
+  [AWS AppConfig](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig.html) 
+  [Creating a configuration and a configuration profile ](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig-creating-configuration-and-profile.html)
+  [About the AppConfig hosted configuration store](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig-creating-configuration-and-profile.html#appconfig-creating-configuration-and-profile-about-hosted-store)