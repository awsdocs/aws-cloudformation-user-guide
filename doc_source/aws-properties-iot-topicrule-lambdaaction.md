# AWS::IoT::TopicRule LambdaAction<a name="aws-properties-iot-topicrule-lambdaaction"></a>

Describes an action to invoke a Lambda function\.

## Syntax<a name="aws-properties-iot-topicrule-lambdaaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-lambdaaction-syntax.json"></a>

```
{
  "[FunctionArn](#cfn-iot-topicrule-lambdaaction-functionarn)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-lambdaaction-syntax.yaml"></a>

```
  [FunctionArn](#cfn-iot-topicrule-lambdaaction-functionarn): String
```

## Properties<a name="aws-properties-iot-topicrule-lambdaaction-properties"></a>

`FunctionArn`  <a name="cfn-iot-topicrule-lambdaaction-functionarn"></a>
The ARN of the Lambda function\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)