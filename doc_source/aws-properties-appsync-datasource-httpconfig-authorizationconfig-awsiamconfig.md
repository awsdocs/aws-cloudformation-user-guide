# AWS AppSync AuthorizationConfig AwsIamConfig<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig"></a>

<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig-description"></a>Use the `AwsIamConfig` property type to specify AwsIamConfig for a AWS AppSync authorizaton\.

<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig-inheritance"></a> `AwsIamConfig` is a property of the [AWS AppSync DataSource AuthorizationConfig](aws-properties-appsync-datasource-httpconfig-authorizationconfig.md) resource\.

## Syntax<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig-syntax.json"></a>

```
{
  "[SigningRegion](#cfn-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig-signingregion)" : String,
  "[SigningServiceName](#cfn-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig-signingservicename)" : String
}
```

### YAML<a name="aws-properties-appsync-datasource-awsiamconfig-syntax.yaml"></a>

```
[SigningRegion](#cfn-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig-signingregion): String
[SigningServiceName](#cfn-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig-signingservicename): String
```

## Properties<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig-properties"></a>

`SigningRegion`  <a name="cfn-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig-signingregion"></a>
The region of signing\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SigningServiceName`  <a name="cfn-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig-signingservicename"></a>
The service name of signing\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-appsync-datasource-httpconfig-authorizationconfig-awsiamconfig-seealso"></a>
+ [ AwsIamConfig](https://docs.aws.amazon.com/appsync/latest/APIReference/API_AwsIamConfig.html) operation in the *AWS AppSync API Reference*