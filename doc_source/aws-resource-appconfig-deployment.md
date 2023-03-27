# AWS::AppConfig::Deployment<a name="aws-resource-appconfig-deployment"></a>

The `AWS::AppConfig::Deployment` resource starts a deployment\. Starting a deployment in AWS AppConfig calls the `StartDeployment` API action\. This call includes the IDs of the AWS AppConfig application, the environment, the configuration profile, and \(optionally\) the configuration data version to deploy\. The call also includes the ID of the deployment strategy to use, which determines how the configuration data is deployed\.

AWS AppConfig monitors the distribution to all hosts and reports status\. If a distribution fails, then AWS AppConfig rolls back the configuration\. 

AWS AppConfig requires that you create resources and deploy a configuration in the following order:

1. Create an application

1. Create an environment

1. Create a configuration profile

1. Create a deployment strategy

1. Deploy the configuration

For more information, see [AWS AppConfig](https://docs.aws.amazon.com/appconfig/latest/userguide/what-is-appconfig.html) in the *AWS AppConfig User Guide*\.

## Syntax<a name="aws-resource-appconfig-deployment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appconfig-deployment-syntax.json"></a>

```
{
  "Type" : "AWS::AppConfig::Deployment",
  "Properties" : {
      "[ApplicationId](#cfn-appconfig-deployment-applicationid)" : String,
      "[ConfigurationProfileId](#cfn-appconfig-deployment-configurationprofileid)" : String,
      "[ConfigurationVersion](#cfn-appconfig-deployment-configurationversion)" : String,
      "[DeploymentStrategyId](#cfn-appconfig-deployment-deploymentstrategyid)" : String,
      "[Description](#cfn-appconfig-deployment-description)" : String,
      "[EnvironmentId](#cfn-appconfig-deployment-environmentid)" : String,
      "[KmsKeyIdentifier](#cfn-appconfig-deployment-kmskeyidentifier)" : String,
      "[Tags](#cfn-appconfig-deployment-tags)" : [ Tags, ... ]
    }
}
```

### YAML<a name="aws-resource-appconfig-deployment-syntax.yaml"></a>

```
Type: AWS::AppConfig::Deployment
Properties: 
  [ApplicationId](#cfn-appconfig-deployment-applicationid): String
  [ConfigurationProfileId](#cfn-appconfig-deployment-configurationprofileid): String
  [ConfigurationVersion](#cfn-appconfig-deployment-configurationversion): String
  [DeploymentStrategyId](#cfn-appconfig-deployment-deploymentstrategyid): String
  [Description](#cfn-appconfig-deployment-description): String
  [EnvironmentId](#cfn-appconfig-deployment-environmentid): String
  [KmsKeyIdentifier](#cfn-appconfig-deployment-kmskeyidentifier): String
  [Tags](#cfn-appconfig-deployment-tags): 
    - Tags
```

## Properties<a name="aws-resource-appconfig-deployment-properties"></a>

`ApplicationId`  <a name="cfn-appconfig-deployment-applicationid"></a>
The application ID\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-z0-9]{4,7}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationProfileId`  <a name="cfn-appconfig-deployment-configurationprofileid"></a>
The configuration profile ID\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-z0-9]{4,7}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationVersion`  <a name="cfn-appconfig-deployment-configurationversion"></a>
The configuration version to deploy\. If deploying an AWS AppConfig hosted configuration version, you can specify either the version number or version label\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeploymentStrategyId`  <a name="cfn-appconfig-deployment-deploymentstrategyid"></a>
The deployment strategy ID\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-z0-9]{4,7}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-appconfig-deployment-description"></a>
A description of the deployment\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnvironmentId`  <a name="cfn-appconfig-deployment-environmentid"></a>
The environment ID\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-z0-9]{4,7}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyIdentifier`  <a name="cfn-appconfig-deployment-kmskeyidentifier"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-appconfig-deployment-tags"></a>
Metadata to assign to the deployment\. Tags help organize and categorize your AWS AppConfig resources\. Each tag consists of a key and an optional value, both of which you define\.  
*Required*: No  
*Type*: [List](aws-properties-appconfig-deployment-tags.md) of [Tags](aws-properties-appconfig-deployment-tags.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-appconfig-deployment-return-values"></a>

### Ref<a name="aws-resource-appconfig-deployment-return-values-ref"></a>

## Examples<a name="aws-resource-appconfig-deployment--examples"></a>



### AWS AppConfig deployment example<a name="aws-resource-appconfig-deployment--examples--_deployment_example"></a>

The following example creates an AWS AppConfig deployment\. Starting a deployment in AWS AppConfig calls the StartDeployment API action\. This call includes the IDs of the AWS AppConfig application, the environment, the configuration profile, and \(optionally\) the configuration data version to deploy\. The call also includes the ID of the deployment strategy to use, which determines how the configuration data is deployed\.

AWS AppConfig monitors the distribution to all hosts and reports status\. If a distribution fails, then AWS AppConfig rolls back the configuration\. 

#### JSON<a name="aws-resource-appconfig-deployment--examples--_deployment_example--json"></a>

```
Resources": {
    "BasicDeployment": {
      "Type": "AWS::AppConfig::Deployment",
      "DependsOn": [
        "MyTestApplication",
        "MyTestConfigurationProfile",
        "MyTestEnvironment",
        "MyTestDeploymentStrategy"
      ],
      "Properties": {
        "ApplicationId": MyTestApplication,
        "EnvironmentId": MyTestEnvironment,
        "DeploymentStrategyId": MyTestDeploymentStrategy,
        "ConfigurationProfileId": MyTestConfigurationProfile,
        "ConfigurationVersion": "1",
        "Description": "My test deployment",
        "Tags": [
          {
            "Key": "Env",
            "Value": "test"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-appconfig-deployment--examples--_deployment_example--yaml"></a>

```
Resources:
  BasicDeployment:
    Type: AWS::AppConfig::Deployment
    Properties:
      ApplicationId: !Ref MyTestApplication
      EnvironmentId: !Ref MyTestEnvironment
      DeploymentStrategyId: !Ref MyTestDeploymentStrategy
      ConfigurationProfileId: !Ref MyTestConfigurationProfile
      ConfigurationVersion: '1'
      Description: 'My test deployment'
      Tags:
        - Key: Env
          Value: test
```

## See also<a name="aws-resource-appconfig-deployment--seealso"></a>
+  [AWS AppConfig](https://docs.aws.amazon.com/appconfig/latest/userguide/what-is-appconfig.html) 
+  [Deploying a configuration](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig-deploying.html)