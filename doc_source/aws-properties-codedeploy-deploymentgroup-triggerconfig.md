# AWS CodeDeploy DeploymentGroup TriggerConfig<a name="aws-properties-codedeploy-deploymentgroup-triggerconfig"></a>

The `TriggerConfig` property type specifies a notification trigger for an AWS CodeDeploy deployment group\. The `TriggerConfigurations` property of the [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md) resource contains a list of `TriggerConfig` property types\.

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-triggerconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-triggerconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentgroup-triggerconfig-triggerevents)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentgroup-triggerconfig-triggername)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentgroup-triggerconfig-triggertargetarn)" : String
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-triggerconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentgroup-triggerconfig-triggerevents): 
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentgroup-triggerconfig-triggername): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentgroup-triggerconfig-triggertargetarn): String
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-triggerconfig-properties"></a>

For more information about each property, including constraints and valid values, see [TriggerConfig](http://docs.aws.amazon.com/codedeploy/latest/APIReference/API_TriggerConfig.html) in the *AWS CodeDeploy API Reference*\.

`TriggerEvents`  
The event type or types that trigger notifications\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`TriggerName`  
The name of the notification trigger\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`TriggerTargetArn`  
The Amazon Resource Name \(ARN\) of the Amazon Simple Notification Service topic through which notifications about deployment or instance events are sent\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption