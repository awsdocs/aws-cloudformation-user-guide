# AWS AppSync GraphQLApi UserPoolConfig<a name="aws-properties-appsync-graphqlapi-userpoolconfig"></a>

<a name="aws-properties-appsync-graphqlapi-userpoolconfig-description"></a>The `UserPoolConfig` property type specifies the optional authorization configuration for using Amazon Cognito User Pools with your GraphQL endpoint for an AWS AppSync GraphQL API\.

<a name="aws-properties-appsync-graphqlapi-userpoolconfig-inheritance"></a> `UserPoolConfig` is a property of the [AWS::AppSync::GraphQLApi](aws-resource-appsync-graphqlapi.md) property type\.

## Syntax<a name="aws-properties-appsync-graphqlapi-userpoolconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-graphqlapi-userpoolconfig-syntax.json"></a>

```
{
  "[AppIdClientRegex](#cfn-appsync-graphqlapi-userpoolconfig-appidclientregex)" : String,
  "[UserPoolId](#cfn-appsync-graphqlapi-userpoolconfig-userpoolid)" : String,
  "[AwsRegion](#cfn-appsync-graphqlapi-userpoolconfig-awsregion)" : String,
  "[DefaultAction](#cfn-appsync-graphqlapi-userpoolconfig-defaultaction)" : String
}
```

### YAML<a name="aws-properties-appsync-graphqlapi-userpoolconfig-syntax.yaml"></a>

```
[AppIdClientRegex](#cfn-appsync-graphqlapi-userpoolconfig-appidclientregex): String
[UserPoolId](#cfn-appsync-graphqlapi-userpoolconfig-userpoolid): String
[AwsRegion](#cfn-appsync-graphqlapi-userpoolconfig-awsregion): String
[DefaultAction](#cfn-appsync-graphqlapi-userpoolconfig-defaultaction): String
```

## Properties<a name="aws-properties-appsync-graphqlapi-userpoolconfig-properties"></a>

`AppIdClientRegex`  <a name="cfn-appsync-graphqlapi-userpoolconfig-appidclientregex"></a>
A regular expression for validating the incoming Amazon Cognito User Pool app client ID\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`UserPoolId`  <a name="cfn-appsync-graphqlapi-userpoolconfig-userpoolid"></a>
The user pool ID\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AwsRegion`  <a name="cfn-appsync-graphqlapi-userpoolconfig-awsregion"></a>
The AWS region in which the user pool was created\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DefaultAction`  <a name="cfn-appsync-graphqlapi-userpoolconfig-defaultaction"></a>
The action that you want your GraphQL API to take when a request that uses Amazon Cognito User Pool authentication doesn't match the Amazon Cognito User Pool configuration\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-appsync-graphqlapi-userpoolconfig-seealso"></a>
+ [ UserPoolConfig](http://docs.aws.amazon.com/appsync/latest/APIReference/API_UserPoolConfig.html) operation in the *AWS AppSync API Reference*