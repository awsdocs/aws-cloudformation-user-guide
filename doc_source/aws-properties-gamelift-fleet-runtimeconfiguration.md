# AWS::GameLift::Fleet RuntimeConfiguration<a name="aws-properties-gamelift-fleet-runtimeconfiguration"></a>

A collection of server process configurations that describe the set of processes to run on each instance in a fleet\. Server processes run either an executable in a custom game build or a Realtime Servers script\. GameLift launches the configured processes, manages their life cycle, and replaces them as needed\. Each instance checks regularly for an updated runtime configuration\. 

A GameLift instance is limited to 50 processes running concurrently\. To calculate the total number of processes in a runtime configuration, add the values of the `ConcurrentExecutions` parameter for each ServerProcess\. Learn more about [ Running Multiple Processes on a Fleet](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-multiprocess.html)\.

## Syntax<a name="aws-properties-gamelift-fleet-runtimeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-fleet-runtimeconfiguration-syntax.json"></a>

```
{
  "[GameSessionActivationTimeoutSeconds](#cfn-gamelift-fleet-runtimeconfiguration-gamesessionactivationtimeoutseconds)" : Integer,
  "[MaxConcurrentGameSessionActivations](#cfn-gamelift-fleet-runtimeconfiguration-maxconcurrentgamesessionactivations)" : Integer,
  "[ServerProcesses](#cfn-gamelift-fleet-runtimeconfiguration-serverprocesses)" : [ ServerProcess, ... ]
}
```

### YAML<a name="aws-properties-gamelift-fleet-runtimeconfiguration-syntax.yaml"></a>

```
  [GameSessionActivationTimeoutSeconds](#cfn-gamelift-fleet-runtimeconfiguration-gamesessionactivationtimeoutseconds): Integer
  [MaxConcurrentGameSessionActivations](#cfn-gamelift-fleet-runtimeconfiguration-maxconcurrentgamesessionactivations): Integer
  [ServerProcesses](#cfn-gamelift-fleet-runtimeconfiguration-serverprocesses): 
    - ServerProcess
```

## Properties<a name="aws-properties-gamelift-fleet-runtimeconfiguration-properties"></a>

`GameSessionActivationTimeoutSeconds`  <a name="cfn-gamelift-fleet-runtimeconfiguration-gamesessionactivationtimeoutseconds"></a>
The maximum amount of time \(in seconds\) allowed to launch a new game session and have it report ready to host players\. During this time, the game session is in status `ACTIVATING`\. If the game session does not become active before the timeout, it is ended and the game session status is changed to `TERMINATED`\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxConcurrentGameSessionActivations`  <a name="cfn-gamelift-fleet-runtimeconfiguration-maxconcurrentgamesessionactivations"></a>
The number of game sessions in status `ACTIVATING` to allow on an instance\. This setting limits the instance resources that can be used for new game activations at any one time\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerProcesses`  <a name="cfn-gamelift-fleet-runtimeconfiguration-serverprocesses"></a>
A collection of server process configurations that identify what server processes to run on each instance in a fleet\.  
*Required*: No  
*Type*: List of [ServerProcess](aws-properties-gamelift-fleet-serverprocess.md)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-gamelift-fleet-runtimeconfiguration--seealso"></a>
+ [ Create GameLift resources using Amazon CloudFront](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [Deploy a GameLift fleet for a custom game build](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-creating.html) in the *Amazon GameLift Developer Guide* 
+  [Deploy a Realtime Servers fleet](https://docs.aws.amazon.com/gamelift/latest/developerguide/realtime-fleets-creating.html) in the *Amazon GameLift Developer Guide* 
+  [Run multiple processes on a fleet](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-multiprocess.html) in the *Amazon GameLift Developer Guide* 
+  [RuntimeConfiguration](https://docs.aws.amazon.com/gamelift/latest/apireference/API_RuntimeConfiguration.html) in the *Amazon GameLift API Reference* 

