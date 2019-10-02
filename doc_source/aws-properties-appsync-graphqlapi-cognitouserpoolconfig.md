# AWS::AppSync::GraphQLApi CognitoUserPoolConfig<a name="aws-properties-appsync-graphqlapi-cognitouserpoolconfig"></a>

Describes an Amazon Cognito user pool configuration\.

## Syntax<a name="aws-properties-appsync-graphqlapi-cognitouserpoolconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-graphqlapi-cognitouserpoolconfig-syntax.json"></a>

```
{
  "[AppIdClientRegex](#cfn-appsync-graphqlapi-cognitouserpoolconfig-appidclientregex)" : String,
  "[AwsRegion](#cfn-appsync-graphqlapi-cognitouserpoolconfig-awsregion)" : String,
  "[UserPoolId](#cfn-appsync-graphqlapi-cognitouserpoolconfig-userpoolid)" : String
}
```

### YAML<a name="aws-properties-appsync-graphqlapi-cognitouserpoolconfig-syntax.yaml"></a>

```
  [AppIdClientRegex](#cfn-appsync-graphqlapi-cognitouserpoolconfig-appidclientregex): String
  [AwsRegion](#cfn-appsync-graphqlapi-cognitouserpoolconfig-awsregion): String
  [UserPoolId](#cfn-appsync-graphqlapi-cognitouserpoolconfig-userpoolid): String
```

## Properties<a name="aws-properties-appsync-graphqlapi-cognitouserpoolconfig-properties"></a>

`AppIdClientRegex`  <a name="cfn-appsync-graphqlapi-cognitouserpoolconfig-appidclientregex"></a>
A regular expression for validating the incoming Amazon Cognito user pool app client ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AwsRegion`  <a name="cfn-appsync-graphqlapi-cognitouserpoolconfig-awsregion"></a>
The AWS Region in which the user pool was created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolId`  <a name="cfn-appsync-graphqlapi-cognitouserpoolconfig-userpoolid"></a>
The user pool ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-2`
