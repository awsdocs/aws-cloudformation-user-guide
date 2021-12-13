# AWS::AppSync::GraphQLApi AdditionalAuthenticationProvider<a name="aws-properties-appsync-graphqlapi-additionalauthenticationprovider"></a>

Describes an additional authentication provider\.

## Syntax<a name="aws-properties-appsync-graphqlapi-additionalauthenticationprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-graphqlapi-additionalauthenticationprovider-syntax.json"></a>

```
{
  "[AuthenticationType](#cfn-appsync-graphqlapi-additionalauthenticationprovider-authenticationtype)" : String,
  "[LambdaAuthorizerConfig](#cfn-appsync-graphqlapi-additionalauthenticationprovider-lambdaauthorizerconfig)" : LambdaAuthorizerConfig,
  "[OpenIDConnectConfig](#cfn-appsync-graphqlapi-additionalauthenticationprovider-openidconnectconfig)" : OpenIDConnectConfig,
  "[UserPoolConfig](#cfn-appsync-graphqlapi-additionalauthenticationprovider-userpoolconfig)" : CognitoUserPoolConfig
}
```

### YAML<a name="aws-properties-appsync-graphqlapi-additionalauthenticationprovider-syntax.yaml"></a>

```
  [AuthenticationType](#cfn-appsync-graphqlapi-additionalauthenticationprovider-authenticationtype): String
  [LambdaAuthorizerConfig](#cfn-appsync-graphqlapi-additionalauthenticationprovider-lambdaauthorizerconfig): 
    LambdaAuthorizerConfig
  [OpenIDConnectConfig](#cfn-appsync-graphqlapi-additionalauthenticationprovider-openidconnectconfig): 
    OpenIDConnectConfig
  [UserPoolConfig](#cfn-appsync-graphqlapi-additionalauthenticationprovider-userpoolconfig): 
    CognitoUserPoolConfig
```

## Properties<a name="aws-properties-appsync-graphqlapi-additionalauthenticationprovider-properties"></a>

`AuthenticationType`  <a name="cfn-appsync-graphqlapi-additionalauthenticationprovider-authenticationtype"></a>
The authentication type for API key, AWS Identity and Access Management, OIDC, Amazon Cognito user pools, or AWS Lambda\.  
Valid Values: `API_KEY` \| `AWS_IAM` \| `OPENID_CONNECT` \| `AMAZON_COGNITO_USER_POOLS` \| `AWS_LAMBDA`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaAuthorizerConfig`  <a name="cfn-appsync-graphqlapi-additionalauthenticationprovider-lambdaauthorizerconfig"></a>
Configuration for AWS Lambda function authorization\.  
*Required*: No  
*Type*: [LambdaAuthorizerConfig](aws-properties-appsync-graphqlapi-lambdaauthorizerconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OpenIDConnectConfig`  <a name="cfn-appsync-graphqlapi-additionalauthenticationprovider-openidconnectconfig"></a>
The OIDC configuration\.  
*Required*: No  
*Type*: [OpenIDConnectConfig](aws-properties-appsync-graphqlapi-openidconnectconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolConfig`  <a name="cfn-appsync-graphqlapi-additionalauthenticationprovider-userpoolconfig"></a>
The Amazon Cognito user pool configuration\.  
*Required*: No  
*Type*: [CognitoUserPoolConfig](aws-properties-appsync-graphqlapi-cognitouserpoolconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)