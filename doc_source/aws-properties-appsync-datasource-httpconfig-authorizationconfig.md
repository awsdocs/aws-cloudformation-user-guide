# AWS AppSync DataSource AuthorizationConfig<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig"></a>

<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-description"></a>The `AuthorizationConfig` property type specifies the authorization type and configuration for an AWS AppSync http data source\.

<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-inheritance"></a> `AuthorizationConfig` is a property of the [AWS AppSync DataSource HttpConfig](aws-properties-appsync-datasource-httpconfig.md) property type\.

## Syntax<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-syntax.json"></a>

```
{
  "[AuthorizationType](#cfn-appsync-datasource-httpconfig-authorizationconfig-authorizationtype)" : String
  "[AwsIamConfig](#cfn-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig)" : [*AwsIamConfig*](aws-properties-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig.md)
}
```

### YAML<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-syntax.yaml"></a>

```
[AuthorizationType](#cfn-appsync-datasource-httpconfig-authorizationconfig-authorizationtype): String
[AwsIamConfig](#cfn-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig): [*AwsIamConfig*](aws-properties-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig.md)
```

## Properties<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-properties"></a>

`AuthorizationType`  <a name="cfn-appsync-datasource-httpconfig-authorizationconfig-authorizationtype"></a>
The type for the Authorization\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AwsIamConfig`  <a name="cfn-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig"></a>
The configuration for the Authorization\.  
 *Required*: No  
 *Type*: [*AwsIamConfig*](aws-properties-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-seealso"></a>
+ [ AuthorizationConfig](https://docs.aws.amazon.com/appsync/latest/APIReference/API_AuthorizationHttpDataSourceConfig.html) operation in the *AWS AppSync API Reference*