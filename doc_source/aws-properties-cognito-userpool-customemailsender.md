# AWS::Cognito::UserPool CustomEmailSender<a name="aws-properties-cognito-userpool-customemailsender"></a>

A custom email sender AWS Lambda trigger\.

## Syntax<a name="aws-properties-cognito-userpool-customemailsender-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-customemailsender-syntax.json"></a>

```
{
  "[LambdaArn](#cfn-cognito-userpool-customemailsender-lambdaarn)" : String,
  "[LambdaVersion](#cfn-cognito-userpool-customemailsender-lambdaversion)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-customemailsender-syntax.yaml"></a>

```
  [LambdaArn](#cfn-cognito-userpool-customemailsender-lambdaarn): String
  [LambdaVersion](#cfn-cognito-userpool-customemailsender-lambdaversion): String
```

## Properties<a name="aws-properties-cognito-userpool-customemailsender-properties"></a>

`LambdaArn`  <a name="cfn-cognito-userpool-customemailsender-lambdaarn"></a>
The Amazon Resource Name \(ARN\) of the AWS Lambda function that Amazon Cognito triggers to send email notifications to users\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaVersion`  <a name="cfn-cognito-userpool-customemailsender-lambdaversion"></a>
The Lambda version represents the signature of the "request" attribute in the "event" information that Amazon Cognito passes to your custom email sender AWS Lambda function\. The only supported value is `V1_0`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)