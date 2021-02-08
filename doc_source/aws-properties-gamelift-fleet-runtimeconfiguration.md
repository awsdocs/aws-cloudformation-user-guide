# AWS::GameLift::Fleet RuntimeConfiguration<a name="aws-properties-gamelift-fleet-runtimeconfiguration"></a>

A collection of server process configurations that describe the processes to run on each instance in a fleet\. All fleets must have a runtime configuration\. Each instance in the fleet maintains server processes as specified in the runtime configuration, launching new ones as existing processes end\. Each instance regularly checks for an updated runtime configuration makes adjustments as called for\. 

The runtime configuration enables the instances in a fleet to run multiple processes simultaneously\. Potential scenarios are as follows: \(1\) Run multiple processes of a single game server executable to maximize usage of your hosting resources\. \(2\) Run one or more processes of different executables, such as your game server and a metrics tracking program\. \(3\) Run multiple processes of a single game server but with different launch parameters, for example to run one process on each instance in debug mode\.

An Amazon GameLift instance is limited to 50 processes running simultaneously\. A runtime configuration must specify fewer than this limit\. To calculate the total number of processes specified in a runtime configuration, add the values of the `ConcurrentExecutions` parameter for each `ServerProcess` object in the runtime configuration\.

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
The maximum amount of time \(in seconds\) that a game session can remain in status `ACTIVATING`\. If the game session is not active before the timeout, activation is terminated and the game session status is changed to `TERMINATED`\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxConcurrentGameSessionActivations`  <a name="cfn-gamelift-fleet-runtimeconfiguration-maxconcurrentgamesessionactivations"></a>
The maximum number of game sessions with status `ACTIVATING` to allow on an instance simultaneously\. This setting limits the amount of instance resources that can be used for new game activations at any one time\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerProcesses`  <a name="cfn-gamelift-fleet-runtimeconfiguration-serverprocesses"></a>
A collection of server process configurations that describe which server processes to run on each instance in a fleet\.  
*Required*: No  
*Type*: List of [ServerProcess](aws-properties-gamelift-fleet-serverprocess.md)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-gamelift-fleet-runtimeconfiguration--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [Deploy a GameLift Fleet for a Custom Game Build](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-creating.html) in the *Amazon GameLift Developer Guide* 
+  [Deploy a Realtime Servers Fleet](https://docs.aws.amazon.com/gamelift/latest/developerguide/realtime-fleets-creating.html) in the *Amazon GameLift Developer Guide* 
+  [Run Multiple Processes on a Fleet](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-multiprocess.html) in the *Amazon GameLift Developer Guide* 
+  [RuntimeConfiguration](https://docs.aws.amazon.com/gamelift/latest/apireference/API_RuntimeConfiguration.html) in the *Amazon GameLift API Reference* 

