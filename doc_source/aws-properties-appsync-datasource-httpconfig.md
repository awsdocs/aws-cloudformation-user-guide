# AWS AppSync DataSource HttpConfig<a name="aws-properties-appsync-datasource-httpconfig"></a>

<a name="aws-properties-appsync-datasource-httpconfig-description"></a>Use the `HttpConfig` property type to specify HttpConfig for an AWS AppSync data source\.

<a name="aws-properties-appsync-datasource-httpconfig-inheritance"></a> `HttpConfig` is a property of the [AWS::AppSync::DataSource](aws-resource-appsync-datasource.md) resource\.

## Syntax<a name="aws-properties-appsync-datasource-httpconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-datasource-httpconfig-syntax.json"></a>

```
{
   "[AuthorizationConfig](#cfn-appsync-datasource-httpconfig-authorizationconfig)" : [*AuthorizationConfig*](aws-properties-appsync-datasource-httpconfig-authorizationconfig.md)
   "[Endpoint](#cfn-appsync-datasource-httpconfig-endpoint)" : String
}
```

### YAML<a name="aws-properties-appsync-datasource-httpconfig-syntax.yaml"></a>

```
[AuthorizationConfig](#cfn-appsync-datasource-httpconfig-authorizationconfig): [*AuthorizationConfig*](aws-properties-appsync-datasource-httpconfig-authorizationconfig.md)
[Endpoint](#cfn-appsync-datasource-httpconfig-endpoint): String
```

## Properties<a name="aws-properties-appsync-datasource-httpconfig-properties"></a>

`AuthorizationConfig`  <a name="cfn-appsync-datasource-httpconfig-authorizationconfig"></a>
The authorization configuration\.  
 *Required*: No  
 *Type*: [*AuthorizationConfig*](aws-properties-appsync-datasource-httpconfig-authorizationconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Endpoint`  <a name="cfn-appsync-datasource-httpconfig-endpoint"></a>
The endpoint\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-appsync-datasource-httpconfig-seealso"></a>
+ [ HttpDataSourceConfig](https://docs.aws.amazon.com/appsync/latest/APIReference/API_HttpDataSourceConfig.html) operation in the *AWS AppSync API Reference*