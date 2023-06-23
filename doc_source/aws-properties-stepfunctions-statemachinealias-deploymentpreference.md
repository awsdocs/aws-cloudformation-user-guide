# AWS::StepFunctions::StateMachineAlias DeploymentPreference<a name="aws-properties-stepfunctions-statemachinealias-deploymentpreference"></a>

Enables gradual state machine deployments\. CloudFormation automatically shifts traffic from the version the alias currently points to, to a new state machine version that you specify\.

## Syntax<a name="aws-properties-stepfunctions-statemachinealias-deploymentpreference-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-stepfunctions-statemachinealias-deploymentpreference-syntax.json"></a>

```
{
  "[Alarms](#cfn-stepfunctions-statemachinealias-deploymentpreference-alarms)" : [ String, ... ],
  "[Interval](#cfn-stepfunctions-statemachinealias-deploymentpreference-interval)" : Integer,
  "[Percentage](#cfn-stepfunctions-statemachinealias-deploymentpreference-percentage)" : Integer,
  "[StateMachineVersionArn](#cfn-stepfunctions-statemachinealias-deploymentpreference-statemachineversionarn)" : String,
  "[Type](#cfn-stepfunctions-statemachinealias-deploymentpreference-type)" : String
}
```

### YAML<a name="aws-properties-stepfunctions-statemachinealias-deploymentpreference-syntax.yaml"></a>

```
  [Alarms](#cfn-stepfunctions-statemachinealias-deploymentpreference-alarms): 
    - String
  [Interval](#cfn-stepfunctions-statemachinealias-deploymentpreference-interval): Integer
  [Percentage](#cfn-stepfunctions-statemachinealias-deploymentpreference-percentage): Integer
  [StateMachineVersionArn](#cfn-stepfunctions-statemachinealias-deploymentpreference-statemachineversionarn): String
  [Type](#cfn-stepfunctions-statemachinealias-deploymentpreference-type): String
```

## Properties<a name="aws-properties-stepfunctions-statemachinealias-deploymentpreference-properties"></a>

`Alarms`  <a name="cfn-stepfunctions-statemachinealias-deploymentpreference-alarms"></a>
A list of Amazon CloudWatch alarms to be monitored during the deployment\. The deployment fails and rolls back if any of these alarms go into the `ALARM` state\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Interval`  <a name="cfn-stepfunctions-statemachinealias-deploymentpreference-interval"></a>
The time in minutes between each traffic shifting increment\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Percentage`  <a name="cfn-stepfunctions-statemachinealias-deploymentpreference-percentage"></a>
The percentage of traffic to shift to the new version in each increment\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StateMachineVersionArn`  <a name="cfn-stepfunctions-statemachinealias-deploymentpreference-statemachineversionarn"></a>
The Amazon Resource Name \(ARN\) of the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-statemachineversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-statemachineversion.html) resource that will be the final version to which the alias points to when the traffic shifting is complete\.  
While performing gradual deployments, you can only provide a single state machine version ARN\. To explicitly set version weights in a CloudFormation template, use `RoutingConfiguration` instead\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-stepfunctions-statemachinealias-deploymentpreference-type"></a>
The type of deployment you want to perform\. You can specify one of the following types:  
+ `LINEAR` \- Shifts traffic to the new version in equal increments with an equal number of seconds between each increment\.

  For example, if you specify the increment percent as `20` with an interval of `600` seconds, this deployment increases traffic by 20 percent every 600 seconds until the new version receives 100 percent of the traffic\. This deployment immediately rolls back the new version if any CloudWatch alarms are triggered\.
+ `ALL_AT_ONCE` \- Shifts 100 percent of traffic to the new version immediately\. CloudFormation monitors the new version and rolls it back automatically to the previous version if any CloudWatch alarms are triggered\.
+ `CANARY` \- Shifts traffic in two increments\.

  In the first increment, a small percentage of traffic, for example, 10 percent is shifted to the new version\. In the second increment, before a specified time interval in seconds gets over, the remaining traffic is shifted to the new version\. The shift to the new version for the remaining traffic takes place only if no CloudWatch alarms are triggered during the specified time interval\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)