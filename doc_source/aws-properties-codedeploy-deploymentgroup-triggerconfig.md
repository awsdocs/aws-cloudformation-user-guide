# AWS::CodeDeploy::DeploymentGroup TriggerConfig<a name="aws-properties-codedeploy-deploymentgroup-triggerconfig"></a>

Information about notification triggers for the deployment group\.

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-triggerconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-triggerconfig-syntax.json"></a>

```
{
  "[TriggerEvents](#cfn-codedeploy-deploymentgroup-triggerconfig-triggerevents)" : [ String, ... ],
  "[TriggerName](#cfn-codedeploy-deploymentgroup-triggerconfig-triggername)" : String,
  "[TriggerTargetArn](#cfn-codedeploy-deploymentgroup-triggerconfig-triggertargetarn)" : String
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-triggerconfig-syntax.yaml"></a>

```
  [TriggerEvents](#cfn-codedeploy-deploymentgroup-triggerconfig-triggerevents): 
    - String
  [TriggerName](#cfn-codedeploy-deploymentgroup-triggerconfig-triggername): String
  [TriggerTargetArn](#cfn-codedeploy-deploymentgroup-triggerconfig-triggertargetarn): String
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-triggerconfig-properties"></a>

`TriggerEvents`  <a name="cfn-codedeploy-deploymentgroup-triggerconfig-triggerevents"></a>
 The event type or types that trigger notifications\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TriggerName`  <a name="cfn-codedeploy-deploymentgroup-triggerconfig-triggername"></a>
The name of the notification trigger\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TriggerTargetArn`  <a name="cfn-codedeploy-deploymentgroup-triggerconfig-triggertargetarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Simple Notification Service topic through which notifications about deployment or instance events are sent\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)