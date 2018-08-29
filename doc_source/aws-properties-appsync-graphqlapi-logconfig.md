# AWS AppSync GraphQLApi LogConfig<a name="aws-properties-appsync-graphqlapi-logconfig"></a>

<a name="aws-properties-appsync-graphqlapi-logconfig-description"></a>The `LogConfig` property type specifies the logging configuration when writing GraphQL operations and tracing to Amazon Cloudwatch for a AWS AppSync GraphQL API\.

<a name="aws-properties-appsync-graphqlapi-logconfig-inheritance"></a> `LogConfig` is a property of the [AWS::AppSync::GraphQLApi](aws-resource-appsync-graphqlapi.md) property type\.

## Syntax<a name="aws-properties-appsync-graphqlapi-logconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-graphqlapi-logconfig-syntax.json"></a>

```
{
  "[CloudWatchLogsRoleArn](#cfn-appsync-graphqlapi-logconfig-cloudwatchlogsrolearn)" : String,
  "[FieldLogLevel](#cfn-appsync-graphqlapi-logconfig-fieldloglevel)" : String
}
```

### YAML<a name="aws-properties-appsync-graphqlapi-logconfig-syntax.yaml"></a>

```
[CloudWatchLogsRoleArn](#cfn-appsync-graphqlapi-logconfig-cloudwatchlogsrolearn): String
[FieldLogLevel](#cfn-appsync-graphqlapi-logconfig-fieldloglevel): String
```

## Properties<a name="aws-properties-appsync-graphqlapi-logconfig-properties"></a>

`CloudWatchLogsRoleArn`  <a name="cfn-appsync-graphqlapi-logconfig-cloudwatchlogsrolearn"></a>
The IAM role that will allow publishing CloudWatch logs into the customer's account\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`FieldLogLevel`  <a name="cfn-appsync-graphqlapi-logconfig-fieldloglevel"></a>
The desired level of logging\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-appsync-graphqlapi-logconfig-seealso"></a>
+ [ LogConfig](http://docs.aws.amazon.com/appsync/latest/APIReference/API_LogConfig.html) operation in the *AWS AppSync API Reference*