# AWS OpsWorks App DataSource<a name="aws-properties-opsworks-app-datasource"></a>

`DataSource` is a property of the [AWS::OpsWorks::App](aws-resource-opsworks-app.md) resource that specifies a database to associate with an AWS OpsWorks app\.

## Syntax<a name="aws-properties-opsworks-app-datasource-syntax"></a>

### JSON<a name="aws-properties-opsworks-app-datasource-syntax.json"></a>

```
{
  "[Arn](#cfn-opsworks-app-datasource-arn)" : String,
  "[DatabaseName](#cfn-opsworks-app-datasource-databasename)" : String,
  "[Type](#cfn-opsworks-app-datasource-type)" : String
}
```

### YAML<a name="aws-properties-opsworks-app-datasource-syntax.yaml"></a>

```
[Arn](#cfn-opsworks-app-datasource-arn): String
[DatabaseName](#cfn-opsworks-app-datasource-databasename): String
[Type](#cfn-opsworks-app-datasource-type): String
```

## Properties<a name="aws-properties-opsworks-app-datasource-properties"></a>

`Arn`  <a name="cfn-opsworks-app-datasource-arn"></a>
The ARN of the data source\.  
*Required*: No  
*Type*: String

`DatabaseName`  <a name="cfn-opsworks-app-datasource-databasename"></a>
The name of the database\.  
*Required*: No  
*Type*: String

`Type`  <a name="cfn-opsworks-app-datasource-type"></a>
The type of the data source, such as `AutoSelectOpsworksMysqlInstance`, `OpsworksMysqlInstance`, or `RdsDbInstance`\. For valid values, see the [DataSource](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_DataSource.html) type in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: No  
*Type*: String