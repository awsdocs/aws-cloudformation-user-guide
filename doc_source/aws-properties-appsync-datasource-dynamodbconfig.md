# AWS AppSync DataSource DynamoDBConfig<a name="aws-properties-appsync-datasource-dynamodbconfig"></a>

<a name="aws-properties-appsync-datasource-dynamodbconfig-description"></a>The `DynamoDBConfig` property type specifies the AwsRegion and TableName for an Amazon DynamoDB table in your account for an AWS AppSync data source\.

<a name="aws-properties-appsync-datasource-dynamodbconfig-inheritance"></a> `DynamoDBConfig` is a property of the [AWS::AppSync::DataSource](aws-resource-appsync-datasource.md) property type\.

## Syntax<a name="aws-properties-appsync-datasource-dynamodbconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-datasource-dynamodbconfig-syntax.json"></a>

```
{
  "[TableName](#cfn-appsync-datasource-dynamodbconfig-tablename)" : String,
  "[AwsRegion](#cfn-appsync-datasource-dynamodbconfig-awsregion)" : String,
  "[UseCallerCredentials](#cfn-appsync-datasource-dynamodbconfig-usecallercredentials)" : Boolean
}
```

### YAML<a name="aws-properties-appsync-datasource-dynamodbconfig-syntax.yaml"></a>

```
[TableName](#cfn-appsync-datasource-dynamodbconfig-tablename): String
[AwsRegion](#cfn-appsync-datasource-dynamodbconfig-awsregion): String
[UseCallerCredentials](#cfn-appsync-datasource-dynamodbconfig-usecallercredentials): Boolean
```

## Properties<a name="aws-properties-appsync-datasource-dynamodbconfig-properties"></a>

`TableName`  <a name="cfn-appsync-datasource-dynamodbconfig-tablename"></a>
The table name\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AwsRegion`  <a name="cfn-appsync-datasource-dynamodbconfig-awsregion"></a>
The AWS region\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`UseCallerCredentials`  <a name="cfn-appsync-datasource-dynamodbconfig-usecallercredentials"></a>
Set to TRUE to use Amazon Cognito credentials with this data source\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-appsync-datasource-dynamodbconfig-seealso"></a>
+ [ DynamodbDataSourceConfig](http://docs.aws.amazon.com/appsync/latest/APIReference/API_DynamodbDataSourceConfig.html) operation in the *AWS AppSync API Reference*