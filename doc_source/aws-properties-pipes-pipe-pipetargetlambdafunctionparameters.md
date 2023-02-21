# AWS::Pipes::Pipe PipeTargetLambdaFunctionParameters<a name="aws-properties-pipes-pipe-pipetargetlambdafunctionparameters"></a>

The parameters for using a Lambda function as a target\.

## Syntax<a name="aws-properties-pipes-pipe-pipetargetlambdafunctionparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipetargetlambdafunctionparameters-syntax.json"></a>

```
{
  "[InvocationType](#cfn-pipes-pipe-pipetargetlambdafunctionparameters-invocationtype)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-pipetargetlambdafunctionparameters-syntax.yaml"></a>

```
  [InvocationType](#cfn-pipes-pipe-pipetargetlambdafunctionparameters-invocationtype): String
```

## Properties<a name="aws-properties-pipes-pipe-pipetargetlambdafunctionparameters-properties"></a>

`InvocationType`  <a name="cfn-pipes-pipe-pipetargetlambdafunctionparameters-invocationtype"></a>
Specify whether to invoke the function synchronously or asynchronously\.  
+ `REQUEST_RESPONSE` \(default\) \- Invoke synchronously\. This corresponds to the `RequestResponse` option in the `InvocationType` parameter for the Lambda [Invoke](https://docs.aws.amazon.com/lambda/latest/dg/API_Invoke.html#API_Invoke_RequestSyntax) API\.
+ `FIRE_AND_FORGET` \- Invoke asynchronously\. This corresponds to the `Event` option in the `InvocationType` parameter for the Lambda [Invoke](https://docs.aws.amazon.com/lambda/latest/dg/API_Invoke.html#API_Invoke_RequestSyntax) API\.
For more information, see [Invocation types](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-pipes.html#pipes-invocation) in the *Amazon EventBridge User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)