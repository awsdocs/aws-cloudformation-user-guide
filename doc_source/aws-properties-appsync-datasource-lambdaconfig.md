# AWS::AppSync::DataSource LambdaConfig<a name="aws-properties-appsync-datasource-lambdaconfig"></a>

The `LambdaConfig` property type specifies the Lambda function ARN for an AWS AppSync data source\.

 `LambdaConfig` is a property of the [AWS::AppSync::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-datasource.html) property type\. 

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
- `us-east-1`
- `us-east-2`
- `us-west-2`
