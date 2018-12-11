# AWS AppSync RelationalDatabase RdsHttpEndpointConfig<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig"></a>

<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-description"></a>Use the `RdsHttpEndpointConfig` property type to specify RdsHttpEndpoint for an AWS AppSync relational database\.

<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-inheritance"></a> `RdsHttpEndpointConfig` is a property of the [AWS AppSync DataSource RelationalDatabaseConfig](aws-properties-appsync-datasource-relationaldatabaseconfig.md) resource\.

## Syntax<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-syntax.json"></a>

```
{
 "[AwsRegion](#cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-awsregion)" : String,
 "[DbClusterIdentifier](#cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-dbclusteridentifier)" : String,
 "[DatabaseName](#cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-databasename)" : String,
 "[Schema](#cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-schema)" : String,
 "[AwsSecretStoreArn](#cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-awssecretstorearn)" : String
}
```

### YAML<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-syntax.yaml"></a>

```
[AwsRegion](#cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-awsregion): String
[DbClusterIdentifier](#cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-dbclusteridentifier): String
[DatabaseName](#cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-databasename): String
[Schema](#cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-schema): String
[AwsSecretStoreArn](#cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-awssecretstorearn): String
```

## Properties<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-properties"></a>

`AwsRegion`  <a name="cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-awsregion"></a>
The aws region of the rdshttpendpoint\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DbClusterIdentifier`  <a name="cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-dbclusteridentifier"></a>
The database cluster identifier of the rdshttpendpoint\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DatabaseName`  <a name="cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-databasename"></a>
The name of the relational database\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Schema`  <a name="cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-schema"></a>
The schema of the relational database\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AwsSecretStoreArn`  <a name="cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-awssecretstorearn"></a>
The secret store ARN of the rdshttpendpoint\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig-seealso"></a>
+ [ RdsHttpEndpointConfig](https://docs.aws.amazon.com/appsync/latest/APIReference/API_RdsHttpEndpointConfig.html) operation in the *AWS AppSync API Reference*