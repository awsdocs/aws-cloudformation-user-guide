# AWS AppSync DataSource RelationalDatabaseConfig<a name="aws-properties-appsync-datasource-relationaldatabaseconfig"></a>

<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-description"></a>Use the `RelationalDatabaseConfig` property type to specify RelationalDatabaseConfig for an AWS AppSync data source\.

<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-inheritance"></a> `RelationalDatabaseConfig` is a property of the [AWS::AppSync::DataSource](aws-resource-appsync-datasource.md) resource\.

## Syntax<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-syntax.json"></a>

```
{
     "[RelationalDatasourceType](#cfn-appsync-datasource-relationaldatabaseconfig-relationaldatasourcetype)" : String,
     "[RdsHttpEndpointConfig](#cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig)" : [*RdsHttpEndpointConfig*](aws-properties-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig.md)
}
```

### YAML<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-syntax.yaml"></a>

```
  [RelationalDatasourceType](#cfn-appsync-datasource-relationaldatabaseconfig-relationaldatasourcetype): String
  [RdsHttpEndpointConfig](#cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig): [*RdsHttpEndpointConfig*](aws-properties-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig.md)
```

## Properties<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-properties"></a>

`RelationalDatasourceType`  <a name="cfn-appsync-datasource-relationaldatabaseconfig-relationaldatasourcetype"></a>
The type of the relational datasource\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RdsHttpEndpointConfig`  <a name="cfn-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig"></a>
The information about the rds resource\.  
 *Required*: No  
 *Type*:[*RdsHttpEndpointConfig*](aws-properties-appsync-datasource-relationaldatabaseconfig-rdshttpendpointconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-appsync-datasource-relationaldatabaseconfig-seealso"></a>
+ [ RelationalDatabaseDataSourceConfig](https://docs.aws.amazon.com/appsync/latest/APIReference/API_RelationalDatabaseDataSourceConfig.html) operation in the *AWS AppSync API Reference*