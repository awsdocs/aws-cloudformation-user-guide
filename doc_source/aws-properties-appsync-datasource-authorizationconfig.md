# AWS::AppSync::DataSource AuthorizationConfig<a name="aws-properties-appsync-datasource-authorizationconfig"></a>

The `AuthorizationConfig` property type specifies the authorization type and configuration for an AWS AppSync http data source\.

 `AuthorizationConfig` is a property of the [AWS AppSync DataSource HttpConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-appsync-datasource-httpconfig.html) property type\. 

## Syntax<a name="aws-properties-appsync-datasource-authorizationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-datasource-authorizationconfig-syntax.json"></a>

```
{
  "[AuthorizationType](#cfn-appsync-datasource-authorizationconfig-authorizationtype)" : String,
  "[AwsIamConfig](#cfn-appsync-datasource-authorizationconfig-awsiamconfig)" : AwsIamConfig
}
```

### YAML<a name="aws-properties-appsync-datasource-authorizationconfig-syntax.yaml"></a>

```
  [AuthorizationType](#cfn-appsync-datasource-authorizationconfig-authorizationtype): String
  [AwsIamConfig](#cfn-appsync-datasource-authorizationconfig-awsiamconfig): 
    AwsIamConfig
```

## Properties<a name="aws-properties-appsync-datasource-authorizationconfig-properties"></a>

`AuthorizationType`  <a name="cfn-appsync-datasource-authorizationconfig-authorizationtype"></a>
The authorization type required by the HTTP endpoint\.  
+  **AWS\_IAM**: The authorization type is Sigv4\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AwsIamConfig`  <a name="cfn-appsync-datasource-authorizationconfig-awsiamconfig"></a>
The AWS IAM settings\.  
*Required*: No  
*Type*: [AwsIamConfig](aws-properties-appsync-datasource-awsiamconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)