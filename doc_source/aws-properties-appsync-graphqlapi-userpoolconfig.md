# AWS::AppSync::GraphQLApi UserPoolConfig<a name="aws-properties-appsync-graphqlapi-userpoolconfig"></a>

The `UserPoolConfig` property type specifies the optional authorization configuration for using Amazon Cognito user pools with your GraphQL endpoint for an AWS AppSync GraphQL API\. 

## Syntax<a name="aws-properties-appsync-graphqlapi-userpoolconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-graphqlapi-userpoolconfig-syntax.json"></a>

```
{
  "[AppIdClientRegex](#cfn-appsync-graphqlapi-userpoolconfig-appidclientregex)" : String,
  "[AwsRegion](#cfn-appsync-graphqlapi-userpoolconfig-awsregion)" : String,
  "[DefaultAction](#cfn-appsync-graphqlapi-userpoolconfig-defaultaction)" : String,
  "[UserPoolId](#cfn-appsync-graphqlapi-userpoolconfig-userpoolid)" : String
}
```

### YAML<a name="aws-properties-appsync-graphqlapi-userpoolconfig-syntax.yaml"></a>

```
  [AppIdClientRegex](#cfn-appsync-graphqlapi-userpoolconfig-appidclientregex): String
  [AwsRegion](#cfn-appsync-graphqlapi-userpoolconfig-awsregion): String
  [DefaultAction](#cfn-appsync-graphqlapi-userpoolconfig-defaultaction): String
  [UserPoolId](#cfn-appsync-graphqlapi-userpoolconfig-userpoolid): String
```

## Properties<a name="aws-properties-appsync-graphqlapi-userpoolconfig-properties"></a>

`AppIdClientRegex`  <a name="cfn-appsync-graphqlapi-userpoolconfig-appidclientregex"></a>
A regular expression for validating the incoming Amazon Cognito user pool app client ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AwsRegion`  <a name="cfn-appsync-graphqlapi-userpoolconfig-awsregion"></a>
The AWS Region in which the user pool was created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultAction`  <a name="cfn-appsync-graphqlapi-userpoolconfig-defaultaction"></a>
The action that you want your GraphQL API to take when a request that uses Amazon Cognito user pool authentication doesn't match the Amazon Cognito user pool configuration\.  
When specifying Cognito user pools as the default authentication, you must set the value for `DefaultAction` to `ALLOW` if specifying `AdditionalAuthenticationProviders`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolId`  <a name="cfn-appsync-graphqlapi-userpoolconfig-userpoolid"></a>
The user pool ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)