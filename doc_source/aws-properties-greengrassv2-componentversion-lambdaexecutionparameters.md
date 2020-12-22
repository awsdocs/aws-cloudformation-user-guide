# AWS::GreengrassV2::ComponentVersion LambdaExecutionParameters<a name="aws-properties-greengrassv2-componentversion-lambdaexecutionparameters"></a>

Contains parameters for a Lambda function that runs on AWS IoT Greengrass\.

## Syntax<a name="aws-properties-greengrassv2-componentversion-lambdaexecutionparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-componentversion-lambdaexecutionparameters-syntax.json"></a>

```
{
  "[EnvironmentVariables](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-environmentvariables)" : {Key : Value, ...},
  "[EventSources](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-eventsources)" : [ LambdaEventSource, ... ],
  "[ExecArgs](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-execargs)" : [ String, ... ],
  "[InputPayloadEncodingType](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-inputpayloadencodingtype)" : String,
  "[LinuxProcessParams](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-linuxprocessparams)" : LambdaLinuxProcessParams,
  "[MaxIdleTimeInSeconds](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-maxidletimeinseconds)" : Integer,
  "[MaxInstancesCount](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-maxinstancescount)" : Integer,
  "[MaxQueueSize](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-maxqueuesize)" : Integer,
  "[Pinned](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-pinned)" : Boolean,
  "[StatusTimeoutInSeconds](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-statustimeoutinseconds)" : Integer,
  "[TimeoutInSeconds](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-timeoutinseconds)" : Integer
}
```

### YAML<a name="aws-properties-greengrassv2-componentversion-lambdaexecutionparameters-syntax.yaml"></a>

```
  [EnvironmentVariables](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-environmentvariables): 
    Key : Value
  [EventSources](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-eventsources): 
    - LambdaEventSource
  [ExecArgs](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-execargs): 
    - String
  [InputPayloadEncodingType](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-inputpayloadencodingtype): String
  [LinuxProcessParams](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-linuxprocessparams): 
    LambdaLinuxProcessParams
  [MaxIdleTimeInSeconds](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-maxidletimeinseconds): Integer
  [MaxInstancesCount](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-maxinstancescount): Integer
  [MaxQueueSize](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-maxqueuesize): Integer
  [Pinned](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-pinned): Boolean
  [StatusTimeoutInSeconds](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-statustimeoutinseconds): Integer
  [TimeoutInSeconds](#cfn-greengrassv2-componentversion-lambdaexecutionparameters-timeoutinseconds): Integer
```

## Properties<a name="aws-properties-greengrassv2-componentversion-lambdaexecutionparameters-properties"></a>

`EnvironmentVariables`  <a name="cfn-greengrassv2-componentversion-lambdaexecutionparameters-environmentvariables"></a>
The map of environment variables that are available to the Lambda function when it runs\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EventSources`  <a name="cfn-greengrassv2-componentversion-lambdaexecutionparameters-eventsources"></a>
The list of event sources to which to subscribe to receive work messages\. The Lambda function runs when it receives a message from an event source\. You can subscribe this function to local publish/subscribe messages and AWS IoT Core MQTT messages\.  
*Required*: No  
*Type*: List of [LambdaEventSource](aws-properties-greengrassv2-componentversion-lambdaeventsource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExecArgs`  <a name="cfn-greengrassv2-componentversion-lambdaexecutionparameters-execargs"></a>
The list of arguments to pass to the Lambda function when it runs\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InputPayloadEncodingType`  <a name="cfn-greengrassv2-componentversion-lambdaexecutionparameters-inputpayloadencodingtype"></a>
The encoding type that the Lambda function supports\.  
Default: `json`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LinuxProcessParams`  <a name="cfn-greengrassv2-componentversion-lambdaexecutionparameters-linuxprocessparams"></a>
The parameters for the Linux process that contains the Lambda function\.  
*Required*: No  
*Type*: [LambdaLinuxProcessParams](aws-properties-greengrassv2-componentversion-lambdalinuxprocessparams.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxIdleTimeInSeconds`  <a name="cfn-greengrassv2-componentversion-lambdaexecutionparameters-maxidletimeinseconds"></a>
The maximum amount of time in seconds that a non\-pinned Lambda function can idle before the AWS IoT Greengrass Core software stops its process\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxInstancesCount`  <a name="cfn-greengrassv2-componentversion-lambdaexecutionparameters-maxinstancescount"></a>
The maximum number of instances that a non\-pinned Lambda function can run at the same time\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxQueueSize`  <a name="cfn-greengrassv2-componentversion-lambdaexecutionparameters-maxqueuesize"></a>
The maximum size of the message queue for the Lambda function component\. The Greengrass core device stores messages in a FIFO \(first\-in\-first\-out\) queue until it can run the Lambda function to consume each message\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Pinned`  <a name="cfn-greengrassv2-componentversion-lambdaexecutionparameters-pinned"></a>
Whether or not the Lambda function is pinned, or long\-lived\.  
+ A pinned Lambda function starts when the AWS IoT Greengrass Core starts and keeps running in its own container\.
+ A non\-pinned Lambda function starts only when it receives a work item and exists after it idles for `maxIdleTimeInSeconds`\. If the function has multiple work items, the AWS IoT Greengrass Core software creates multiple instances of the function\.
Default: `true`  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StatusTimeoutInSeconds`  <a name="cfn-greengrassv2-componentversion-lambdaexecutionparameters-statustimeoutinseconds"></a>
The interval in seconds at which a pinned \(also known as long\-lived\) Lambda function component sends status updates to the Lambda manager component\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TimeoutInSeconds`  <a name="cfn-greengrassv2-componentversion-lambdaexecutionparameters-timeoutinseconds"></a>
The maximum amount of time in seconds that the Lambda function can process a work item\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)