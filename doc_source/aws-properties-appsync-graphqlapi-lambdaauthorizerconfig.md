# AWS::AppSync::GraphQLApi LambdaAuthorizerConfig<a name="aws-properties-appsync-graphqlapi-lambdaauthorizerconfig"></a>

Configuration for AWS Lambda function authorization\.

## Syntax<a name="aws-properties-appsync-graphqlapi-lambdaauthorizerconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-graphqlapi-lambdaauthorizerconfig-syntax.json"></a>

```
{
  "[AuthorizerResultTtlInSeconds](#cfn-appsync-graphqlapi-lambdaauthorizerconfig-authorizerresultttlinseconds)" : Double,
  "[AuthorizerUri](#cfn-appsync-graphqlapi-lambdaauthorizerconfig-authorizeruri)" : String,
  "[IdentityValidationExpression](#cfn-appsync-graphqlapi-lambdaauthorizerconfig-identityvalidationexpression)" : String
}
```

### YAML<a name="aws-properties-appsync-graphqlapi-lambdaauthorizerconfig-syntax.yaml"></a>

```
  [AuthorizerResultTtlInSeconds](#cfn-appsync-graphqlapi-lambdaauthorizerconfig-authorizerresultttlinseconds): Double
  [AuthorizerUri](#cfn-appsync-graphqlapi-lambdaauthorizerconfig-authorizeruri): String
  [IdentityValidationExpression](#cfn-appsync-graphqlapi-lambdaauthorizerconfig-identityvalidationexpression): String
```

## Properties<a name="aws-properties-appsync-graphqlapi-lambdaauthorizerconfig-properties"></a>

`AuthorizerResultTtlInSeconds`  <a name="cfn-appsync-graphqlapi-lambdaauthorizerconfig-authorizerresultttlinseconds"></a>
The number of seconds a response should be cached for\. The default is 5 minutes \(300 seconds\)\. The Lambda function can override this by returning a `ttlOverride` key in its response\. A value of 0 disables caching of responses\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizerUri`  <a name="cfn-appsync-graphqlapi-lambdaauthorizerconfig-authorizeruri"></a>
The ARN of the Lambda function to be called for authorization\. This may be a standard Lambda ARN, a version ARN \(`.../v3`\) or alias ARN\.   
*Note*: This Lambda function must have the following resource\-based policy assigned to it\. When configuring Lambda authorizers in the console, this is done for you\. To do so with the AWS CLI, run the following:  
`aws lambda add-permission --function-name "arn:aws:lambda:us-east-2:111122223333:function:my-function" --statement-id "appsync" --principal appsync.amazonaws.com --action lambda:InvokeFunction`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityValidationExpression`  <a name="cfn-appsync-graphqlapi-lambdaauthorizerconfig-identityvalidationexpression"></a>
A regular expression for validation of tokens before the Lambda function is called\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)