# AWS::AppSync::GraphQLApi LogConfig<a name="aws-properties-appsync-graphqlapi-logconfig"></a>

The `LogConfig` property type specifies the logging configuration when writing GraphQL operations and tracing to Amazon CloudWatch for a AWS AppSync GraphQL API\.

 `LogConfig` is a property of the [AWS::AppSync::GraphQLApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-graphqlapi.html) property type\. 

## Syntax<a name="aws-properties-appsync-graphqlapi-logconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-graphqlapi-logconfig-syntax.json"></a>

```
{
  "[CloudWatchLogsRoleArn](#cfn-appsync-graphqlapi-logconfig-cloudwatchlogsrolearn)" : String,
  "[ExcludeVerboseContent](#cfn-appsync-graphqlapi-logconfig-excludeverbosecontent)" : Boolean,
  "[FieldLogLevel](#cfn-appsync-graphqlapi-logconfig-fieldloglevel)" : String
}
```

### YAML<a name="aws-properties-appsync-graphqlapi-logconfig-syntax.yaml"></a>

```
  [CloudWatchLogsRoleArn](#cfn-appsync-graphqlapi-logconfig-cloudwatchlogsrolearn): String
  [ExcludeVerboseContent](#cfn-appsync-graphqlapi-logconfig-excludeverbosecontent): Boolean
  [FieldLogLevel](#cfn-appsync-graphqlapi-logconfig-fieldloglevel): String
```

## Properties<a name="aws-properties-appsync-graphqlapi-logconfig-properties"></a>

`CloudWatchLogsRoleArn`  <a name="cfn-appsync-graphqlapi-logconfig-cloudwatchlogsrolearn"></a>
The service role that AWS AppSync will assume to publish to Amazon CloudWatch Logs in your account\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeVerboseContent`  <a name="cfn-appsync-graphqlapi-logconfig-excludeverbosecontent"></a>
Set to TRUE to exclude sections that contain information such as headers, context, and evaluated mapping templates, regardless of logging level\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldLogLevel`  <a name="cfn-appsync-graphqlapi-logconfig-fieldloglevel"></a>
The field logging level\. Values can be NONE, ERROR, or ALL\.   
+  **NONE**: No field\-level logs are captured\.
+  **ERROR**: Logs the following information only for the fields that are in error:
  + The error section in the server response\.
  + Field\-level errors\.
  + The generated request/response functions that got resolved for error fields\.
+  **ALL**: The following information is logged for all fields in the query:
  + Field\-level tracing information\.
  + The generated request/response functions that got resolved for each field\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)