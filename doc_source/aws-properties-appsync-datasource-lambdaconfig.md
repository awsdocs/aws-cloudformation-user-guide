# AWS AppSync DataSource LambdaConfig<a name="aws-properties-appsync-datasource-lambdaconfig"></a>

<a name="aws-properties-appsync-datasource-lambdaconfig-description"></a>The `LambdaConfig` property type specifies the Lambda function ARN for an AWS AppSync data source\.

<a name="aws-properties-appsync-datasource-lambdaconfig-inheritance"></a> `LambdaConfig` is a property of the [AWS::AppSync::DataSource](aws-resource-appsync-datasource.md) property type\.

## Syntax<a name="aws-properties-appsync-datasource-lambdaconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-datasource-lambdaconfig-syntax.json"></a>

```
{
  "[LambdaFunctionArn](#cfn-appsync-datasource-lambdaconfig-lambdafunctionarn)" : String
}
```

### YAML<a name="aws-properties-appsync-datasource-lambdaconfig-syntax.yaml"></a>

```
[LambdaFunctionArn](#cfn-appsync-datasource-lambdaconfig-lambdafunctionarn): String
```

## Properties<a name="aws-properties-appsync-datasource-lambdaconfig-properties"></a>

`LambdaFunctionArn`  <a name="cfn-appsync-datasource-lambdaconfig-lambdafunctionarn"></a>
The ARN for the Lambda function\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-appsync-datasource-lambdaconfig-seealso"></a>
+ [ LambdaDataSourceConfig](http://docs.aws.amazon.com/appsync/latest/APIReference/API_LambdaDataSourceConfig.html) operation in the *AWS AppSync API Reference*