# AWS::OpsWorks::App DataSource<a name="aws-properties-opsworks-app-datasource"></a>

Describes an app's data source\.

## Syntax<a name="aws-properties-opsworks-app-datasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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
The data source's ARN\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-opsworks-app-datasource-databasename"></a>
The database name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-opsworks-app-datasource-type"></a>
The data source's type, `AutoSelectOpsworksMysqlInstance`, `OpsworksMysqlInstance`, `RdsDbInstance`, or `None`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)