# AWS::StepFunctions::StateMachineAlias<a name="aws-resource-stepfunctions-statemachinealias"></a>

Represents a state machine [alias](https://docs.aws.amazon.com/step-functions/latest/dg/concepts-state-machine-alias.html)\. An alias routes traffic to one or two versions of the same state machine\.

You can create up to 100 aliases for each state machine\.

## Syntax<a name="aws-resource-stepfunctions-statemachinealias-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-stepfunctions-statemachinealias-syntax.json"></a>

```
{
  "Type" : "AWS::StepFunctions::StateMachineAlias",
  "Properties" : {
      "[DeploymentPreference](#cfn-stepfunctions-statemachinealias-deploymentpreference)" : DeploymentPreference,
      "[Description](#cfn-stepfunctions-statemachinealias-description)" : String,
      "[Name](#cfn-stepfunctions-statemachinealias-name)" : String,
      "[RoutingConfiguration](#cfn-stepfunctions-statemachinealias-routingconfiguration)" : [ RoutingConfigurationVersion, ... ]
    }
}
```

### YAML<a name="aws-resource-stepfunctions-statemachinealias-syntax.yaml"></a>

```
Type: AWS::StepFunctions::StateMachineAlias
Properties: 
  [DeploymentPreference](#cfn-stepfunctions-statemachinealias-deploymentpreference): 
    DeploymentPreference
  [Description](#cfn-stepfunctions-statemachinealias-description): String
  [Name](#cfn-stepfunctions-statemachinealias-name): String
  [RoutingConfiguration](#cfn-stepfunctions-statemachinealias-routingconfiguration): 
    - RoutingConfigurationVersion
```

## Properties<a name="aws-resource-stepfunctions-statemachinealias-properties"></a>

`DeploymentPreference`  <a name="cfn-stepfunctions-statemachinealias-deploymentpreference"></a>
The settings that enable gradual state machine deployments\. These settings include [Alarms](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stepfunctions-statemachinealias-deploymentpreference.html#cfn-stepfunctions-statemachinealias-deploymentpreference-alarms), [Interval](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stepfunctions-statemachinealias-deploymentpreference.html#cfn-stepfunctions-statemachinealias-deploymentpreference-interval), [Percentage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stepfunctions-statemachinealias-deploymentpreference.html#cfn-stepfunctions-statemachinealias-deploymentpreference-percentage), [StateMachineVersionArn](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stepfunctions-statemachinealias-deploymentpreference.html#cfn-stepfunctions-statemachinealias-deploymentpreference-statemachineversionarn), and [Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stepfunctions-statemachinealias-deploymentpreference.html#cfn-stepfunctions-statemachinealias-deploymentpreference-type)\.  
CloudFormation automatically shifts traffic from the version an alias currently points to, to a new state machine version that you specify\.  
`RoutingConfiguration` and `DeploymentPreference` are mutually exclusive properties\. You must define only one of these properties\.
Based on the type of deployment you want to perform, you can specify one of the following settings:  
+ `LINEAR` \- Shifts traffic to the new version in equal increments with an equal number of seconds between each increment\.

  For example, if you specify the increment percent as `20` with an interval of `600` seconds, this deployment increases traffic by 20 percent every 600 seconds until the new version receives 100 percent of the traffic\. This deployment immediately rolls back the new version if any Amazon CloudWatch alarms are triggered\.
+ `ALL_AT_ONCE` \- Shifts 100 percent of traffic to the new version immediately\. CloudFormation monitors the new version and rolls it back automatically to the previous version if any CloudWatch alarms are triggered\.
+ `CANARY` \- Shifts traffic in two increments\.

  In the first increment, a small percentage of traffic, for example, 10 percent is shifted to the new version\. In the second increment, before a specified time interval in seconds gets over, the remaining traffic is shifted to the new version\. The shift to the new version for the remaining traffic takes place only if no CloudWatch alarms are triggered during the specified time interval\.
*Required*: No  
*Type*: [DeploymentPreference](aws-properties-stepfunctions-statemachinealias-deploymentpreference.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-stepfunctions-statemachinealias-description"></a>
An optional description of the state machine alias\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-stepfunctions-statemachinealias-name"></a>
The name of the state machine alias\. If you don't provide a name, it uses an automatically generated name based on the logical ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoutingConfiguration`  <a name="cfn-stepfunctions-statemachinealias-routingconfiguration"></a>
The routing configuration of an alias\. Routing configuration splits [StartExecution](https://docs.aws.amazon.com/step-functions/latest/apireference/API_StartExecution.html) requests between one or two versions of the same state machine\.  
Use `RoutingConfiguration` if you want to explicitly set the alias [weights](https://docs.aws.amazon.com/step-functions/latest/apireference/API_RoutingConfigurationListItem.html#StepFunctions-Type-RoutingConfigurationListItem-weight)\. Weight is the percentage of traffic you want to route to a state machine version\.  
`RoutingConfiguration` and `DeploymentPreference` are mutually exclusive properties\. You must define only one of these properties\.
*Required*: No  
*Type*: List of [RoutingConfigurationVersion](aws-properties-stepfunctions-statemachinealias-routingconfigurationversion.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-stepfunctions-statemachinealias-return-values"></a>

### Ref<a name="aws-resource-stepfunctions-statemachinealias-return-values-ref"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the ARN of the created state machine alias\. For example,

```
{ "Ref": "PROD" }
```

Returns the ARN of the created state machine alias as shown in the following example\.

`arn:aws:states:us-east-1:123456789012:stateMachine:myStateMachine:PROD`

For more information about using `Ref`, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-stepfunctions-statemachinealias-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following is the available attribute\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-stepfunctions-statemachinealias-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the ARN of the state machine alias\. For example, `arn:aws:states:us-east-1:123456789012:stateMachine:myStateMachine:PROD`\.

## Examples<a name="aws-resource-stepfunctions-statemachinealias--examples"></a>

The following are examples of `LINEAR` deployment that show how you can use an alias to shift traffic to a new version\. The first example snippet shows an alias named `PROD` that shifts 20 percent of traffic to the version B every five minutes\.

The second example shows how you can publish multiple versions of the same state machine with the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-statemachineversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-statemachineversion.html) resource, create an alias with the `AWS::StepFunctions::Alias` resource, and use the alias to deploy a new version\.

### Shifting traffic to a new version with an alias<a name="aws-resource-stepfunctions-statemachinealias--examples--Shifting_traffic_to_a_new_version_with_an_alias"></a>

#### YAML<a name="aws-resource-stepfunctions-statemachinealias--examples--Shifting_traffic_to_a_new_version_with_an_alias--yaml"></a>

```
PROD:
  Type: AWS::StepFunctions::Alias
  Properties:
    Name: PROD
    Description: The PROD state machine alias taking production traffic.
    DeploymentPreference:
      StateMachineVersionArn: !Ref MyStateMachineVersionB
      Type: LINEAR
      Interval: 5
      Percentage: 20
      Alarms:
        # A list of alarms that you want to monitor
        - !Ref AliasErrorMetricGreaterThanZeroAlarm
        - !Ref LatestVersionErrorMetricGreaterThanZeroAlarm
```

### Complete example to publish and deploy a new version with an alias<a name="aws-resource-stepfunctions-statemachinealias--examples--Complete_example_to_publish_and_deploy_a_new_version_with_an_alias"></a>

#### YAML<a name="aws-resource-stepfunctions-statemachinealias--examples--Complete_example_to_publish_and_deploy_a_new_version_with_an_alias--yaml"></a>

```
MyStateMachine:
  Type: AWS::StepFunctions::StateMachine
  Properties:
    Type: STANDARD
    StateMachineName: MyStateMachine
    RoleArn: arn:aws:iam::12345678912:role/myIamRole
    Definition:
      StartAt: PassState
      States:
        PassState:
          Type: Pass
          Result: Result
          End: true

MyStateMachineVersionA:
  Type: AWS::StepFunctions::StateMachineVersion
  Properties:
    Description: Version 1
    StateMachineArn: !Ref MyStateMachine

MyStateMachineVersionB:
  Type: AWS::StepFunctions::StateMachineVersion
  Properties:
    Description: Version 2
    StateMachineArn: !Ref MyStateMachine

PROD:
  Type: AWS::StepFunctions::StateMachineAlias
  Properties:
    Name: PROD
    Description: The PROD state machine alias taking production traffic.
    DeploymentPreference:
      VersionArn: !Ref MyStateMachineVersionB
      Type: LINEAR
      Percentage: 20
      Interval: 5
      Alarms:
        - !Ref CloudWatchAlarm1
        - !Ref CloudWatchAlarm2
```