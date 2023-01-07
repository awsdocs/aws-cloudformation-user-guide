# AWS::IoT::TopicRule StepFunctionsAction<a name="aws-properties-iot-topicrule-stepfunctionsaction"></a>

Starts execution of a Step Functions state machine\.

## Syntax<a name="aws-properties-iot-topicrule-stepfunctionsaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-stepfunctionsaction-syntax.json"></a>

```
{
  "[ExecutionNamePrefix](#cfn-iot-topicrule-stepfunctionsaction-executionnameprefix)" : String,
  "[RoleArn](#cfn-iot-topicrule-stepfunctionsaction-rolearn)" : String,
  "[StateMachineName](#cfn-iot-topicrule-stepfunctionsaction-statemachinename)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-stepfunctionsaction-syntax.yaml"></a>

```
  [ExecutionNamePrefix](#cfn-iot-topicrule-stepfunctionsaction-executionnameprefix): String
  [RoleArn](#cfn-iot-topicrule-stepfunctionsaction-rolearn): String
  [StateMachineName](#cfn-iot-topicrule-stepfunctionsaction-statemachinename): String
```

## Properties<a name="aws-properties-iot-topicrule-stepfunctionsaction-properties"></a>

`ExecutionNamePrefix`  <a name="cfn-iot-topicrule-stepfunctionsaction-executionnameprefix"></a>
\(Optional\) A name will be given to the state machine execution consisting of this prefix followed by a UUID\. Step Functions automatically creates a unique name for each state machine execution if one is not provided\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-stepfunctionsaction-rolearn"></a>
The ARN of the role that grants IoT permission to start execution of a state machine \("Action":"states:StartExecution"\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StateMachineName`  <a name="cfn-iot-topicrule-stepfunctionsaction-statemachinename"></a>
The name of the Step Functions state machine whose execution will be started\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-iot-topicrule-stepfunctionsaction--seealso"></a>
+  [StepFunctionsAction](https://docs.aws.amazon.com/iot/latest/apireference/API_StepFunctionsAction.html) in the *AWS IoT API Reference*\.

