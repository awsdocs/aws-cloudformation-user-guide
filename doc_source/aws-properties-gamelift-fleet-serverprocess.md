# AWS::GameLift::Fleet ServerProcess<a name="aws-properties-gamelift-fleet-serverprocess"></a>

A set of instructions for launching server processes on each instance in a fleet\. Each instruction set identifies the location of the server executable, optional launch parameters, and the number of server processes with this configuration to maintain concurrently on the instance\. Server process configurations make up a fleet's `RuntimeConfiguration`\.

## Syntax<a name="aws-properties-gamelift-fleet-serverprocess-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-fleet-serverprocess-syntax.json"></a>

```
{
  "[ConcurrentExecutions](#cfn-gamelift-fleet-serverprocess-concurrentexecutions)" : Integer,
  "[LaunchPath](#cfn-gamelift-fleet-serverprocess-launchpath)" : String,
  "[Parameters](#cfn-gamelift-fleet-serverprocess-parameters)" : String
}
```

### YAML<a name="aws-properties-gamelift-fleet-serverprocess-syntax.yaml"></a>

```
  [ConcurrentExecutions](#cfn-gamelift-fleet-serverprocess-concurrentexecutions): Integer
  [LaunchPath](#cfn-gamelift-fleet-serverprocess-launchpath): String
  [Parameters](#cfn-gamelift-fleet-serverprocess-parameters): String
```

## Properties<a name="aws-properties-gamelift-fleet-serverprocess-properties"></a>

`ConcurrentExecutions`  <a name="cfn-gamelift-fleet-serverprocess-concurrentexecutions"></a>
The number of server processes that use this configuration to run concurrently on an instance\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchPath`  <a name="cfn-gamelift-fleet-serverprocess-launchpath"></a>
The location of the server executable in a custom game build or the name of the Realtime script file that contains the `Init()` function\. Game builds and Realtime scripts are installed on instances at the root:   
+ Windows \(for custom game builds only\): `C:\game`\. Example: "`C:\game\MyGame\server.exe`" 
+ Linux: `/local/game`\. Examples: "`/local/game/MyGame/server.exe`" or "`/local/game/MyRealtimeScript.js`"
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-gamelift-fleet-serverprocess-parameters"></a>
An optional list of parameters to pass to the server executable or Realtime script on launch\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-gamelift-fleet-serverprocess--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [Deploy a GameLift Fleet for a Custom Game Build](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-creating.html) in the *Amazon GameLift Developer Guide* 
+  [Deploy a Realtime Servers Fleet](https://docs.aws.amazon.com/gamelift/latest/developerguide/realtime-fleets-creating.html) in the *Amazon GameLift Developer Guide* 
+  [Run Multiple Processes on a Fleet](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-multiprocess.html) in the *Amazon GameLift Developer Guide* 
+  [ServerProcess](https://docs.aws.amazon.com/gamelift/latest/apireference/API_ServerProcess.html) in the *Amazon GameLift API Reference* 

