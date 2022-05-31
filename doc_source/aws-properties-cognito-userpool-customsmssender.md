# AWS::Cognito::UserPool CustomSMSSender<a name="aws-properties-cognito-userpool-customsmssender"></a>

A custom SMS sender AWS Lambda trigger\.

## Syntax<a name="aws-properties-cognito-userpool-customsmssender-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-customsmssender-syntax.json"></a>

```
{
  "[LambdaArn](#cfn-cognito-userpool-customsmssender-lambdaarn)" : String,
  "[LambdaVersion](#cfn-cognito-userpool-customsmssender-lambdaversion)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-customsmssender-syntax.yaml"></a>

```
  [LambdaArn](#cfn-cognito-userpool-customsmssender-lambdaarn): String
  [LambdaVersion](#cfn-cognito-userpool-customsmssender-lambdaversion): String
```

## Properties<a name="aws-properties-cognito-userpool-customsmssender-properties"></a>

`LambdaArn`  <a name="cfn-cognito-userpool-customsmssender-lambdaarn"></a>
The Amazon Resource Name \(ARN\) of the AWS Lambda function that Amazon Cognito triggers to send SMS notifications to users\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaVersion`  <a name="cfn-cognito-userpool-customsmssender-lambdaversion"></a>
The Lambda version represents the signature of the "request" attribute in the "event" information Amazon Cognito passes to your custom SMS sender Lambda function\. The only supported value is `V1_0`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)