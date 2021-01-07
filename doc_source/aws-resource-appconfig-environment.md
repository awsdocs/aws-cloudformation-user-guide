# AWS::AppConfig::Environment<a name="aws-resource-appconfig-environment"></a>

The `AWS::AppConfig::Environment` resource creates an environment, which is a logical deployment group of AppConfig targets, such as applications in a `Beta` or `Production` environment\. You define one or more environments for each AppConfig application\. You can also define environments for application subcomponents such as the `Web`, `Mobile` and `Back-end` components for your application\. You can configure Amazon CloudWatch alarms for each environment\. The system monitors alarms during a configuration deployment\. If an alarm is triggered, the system rolls back the configuration\.

AppConfig requires that you create resources and deploy a configuration in the following order:

1. Create an application

1. Create an environment

1. Create a configuration profile

1. Create a deployment strategy

1. Deploy the configuration

For more information, see [AWS AppConfig](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig.html) in the *AWS Systems Manager User Guide*\.

## Syntax<a name="aws-resource-appconfig-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appconfig-environment-syntax.json"></a>

```
{
  "Type" : "AWS::AppConfig::Environment",
  "Properties" : {
      "[ApplicationId](#cfn-appconfig-environment-applicationid)" : String,
      "[Description](#cfn-appconfig-environment-description)" : String,
      "[Monitors](#cfn-appconfig-environment-monitors)" : [ Monitors, ... ],
      "[Name](#cfn-appconfig-environment-name)" : String,
      "[Tags](#cfn-appconfig-environment-tags)" : [ Tags, ... ]
    }
}
```

### YAML<a name="aws-resource-appconfig-environment-syntax.yaml"></a>

```
Type: AWS::AppConfig::Environment
Properties: 
  [ApplicationId](#cfn-appconfig-environment-applicationid): String
  [Description](#cfn-appconfig-environment-description): String
  [Monitors](#cfn-appconfig-environment-monitors): 
    - Monitors
  [Name](#cfn-appconfig-environment-name): String
  [Tags](#cfn-appconfig-environment-tags): 
    - Tags
```

## Properties<a name="aws-resource-appconfig-environment-properties"></a>

`ApplicationId`  <a name="cfn-appconfig-environment-applicationid"></a>
The application ID\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-z0-9]{4,7}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-appconfig-environment-description"></a>
A description of the environment\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Monitors`  <a name="cfn-appconfig-environment-monitors"></a>
Amazon CloudWatch alarms to monitor during the deployment process\.  
*Required*: No  
*Type*: [List](aws-properties-appconfig-environment-monitors.md) of [Monitors](aws-properties-appconfig-environment-monitors.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appconfig-environment-name"></a>
A name for the environment\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appconfig-environment-tags"></a>
Metadata to assign to the environment\. Tags help organize and categorize your AWS AppConfig resources\. Each tag consists of a key and an optional value, both of which you define\.  
*Required*: No  
*Type*: [List](aws-properties-appconfig-environment-tags.md) of [Tags](aws-properties-appconfig-environment-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appconfig-environment-return-values"></a>

### Ref<a name="aws-resource-appconfig-environment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the environment ID\.

## Examples<a name="aws-resource-appconfig-environment--examples"></a>



### AWS AppConfig Environment Example<a name="aws-resource-appconfig-environment--examples--AWS_AppConfig_Environment_Example"></a>

The following example creates an AWS AppConfig environment named MyTestEnvironment\. An environment is a logical deployment group of AppConfig targets, such as applications in a Beta or Production environment\. You can also define environments for application subcomponents such as the Web, Mobile, and Back\-end components for your application\. 

#### JSON<a name="aws-resource-appconfig-environment--examples--AWS_AppConfig_Environment_Example--json"></a>

```
Resources": {
    "BasicEnvironment": {
      "Type": "AWS::AppConfig::Environment",
      "DependsOn": "DependentApplication",
      "Properties": {
        "ApplicationId": null,
        "Name": "MyTestEnvironment",
        "Description": "My test environment",
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

#### YAML<a name="aws-resource-appconfig-environment--examples--AWS_AppConfig_Environment_Example--yaml"></a>

```
Resources:
  BasicEnvironment:
    Type: AWS::AppConfig::Environment
    Properties:
      ApplicationId: !Ref DependentApplication
      Name: "MyTestEnvironment"
      Description: "My test environment"
      Tags:
        - Key: Env
          Value: test
```

## See also<a name="aws-resource-appconfig-environment--seealso"></a>
+  [AWS AppConfig](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig.html) 
+  [Creating an environment](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig-creating-environment.html)