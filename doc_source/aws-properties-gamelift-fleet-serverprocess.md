# AWS::GameLift::Fleet ServerProcess<a name="aws-properties-gamelift-fleet-serverprocess"></a>

A set of instructions for launching server processes on each instance in a fleet\. Server processes run either an executable in a custom game build or a Realtime Servers script\. 

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
The number of server processes using this configuration that run concurrently on each instance\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchPath`  <a name="cfn-gamelift-fleet-serverprocess-launchpath"></a>
The location of a game build executable or the Realtime script file that contains the `Init()` function\. Game builds and Realtime scripts are installed on instances at the root:   
+ Windows \(custom game builds only\): `C:\game`\. Example: "`C:\game\MyGame\server.exe`" 
+ Linux: `/local/game`\. Examples: "`/local/game/MyGame/server.exe`" or "`/local/game/MyRealtimeScript.js`"
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `[A-Za-z0-9_:.+\/\\\- ]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-gamelift-fleet-serverprocess-parameters"></a>
An optional list of parameters to pass to the server executable or Realtime script on launch\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `[A-Za-z0-9_:.+\/\\\- =@;{},?'\[\]"]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-gamelift-fleet-serverprocess--seealso"></a>
+ [ Create GameLift resources using Amazon CloudFront](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [Deploy a GameLift fleet for a custom game build](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-creating.html) in the *Amazon GameLift Developer Guide* 
+  [Deploy a Realtime Servers fleet](https://docs.aws.amazon.com/gamelift/latest/developerguide/realtime-fleets-creating.html) in the *Amazon GameLift Developer Guide* 
+  [Run multiple processes on a fleet](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-multiprocess.html) in the *Amazon GameLift Developer Guide* 
+  [ServerProcess](https://docs.aws.amazon.com/gamelift/latest/apireference/API_ServerProcess.html) in the *Amazon GameLift API Reference* 

