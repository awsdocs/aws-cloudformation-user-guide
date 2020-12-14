# AWS::Kendra::DataSource DatabaseConfiguration<a name="aws-properties-kendra-datasource-databaseconfiguration"></a>

Provides the information necessary to connect a database to an index\. 

## Syntax<a name="aws-properties-kendra-datasource-databaseconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-databaseconfiguration-syntax.json"></a>

```
{
  "[AclConfiguration](#cfn-kendra-datasource-databaseconfiguration-aclconfiguration)" : AclConfiguration,
  "[ColumnConfiguration](#cfn-kendra-datasource-databaseconfiguration-columnconfiguration)" : ColumnConfiguration,
  "[ConnectionConfiguration](#cfn-kendra-datasource-databaseconfiguration-connectionconfiguration)" : ConnectionConfiguration,
  "[DatabaseEngineType](#cfn-kendra-datasource-databaseconfiguration-databaseenginetype)" : String,
  "[SqlConfiguration](#cfn-kendra-datasource-databaseconfiguration-sqlconfiguration)" : SqlConfiguration,
  "[VpcConfiguration](#cfn-kendra-datasource-databaseconfiguration-vpcconfiguration)" : DataSourceVpcConfiguration
}
```

### YAML<a name="aws-properties-kendra-datasource-databaseconfiguration-syntax.yaml"></a>

```
  [AclConfiguration](#cfn-kendra-datasource-databaseconfiguration-aclconfiguration): 
    AclConfiguration
  [ColumnConfiguration](#cfn-kendra-datasource-databaseconfiguration-columnconfiguration): 
    ColumnConfiguration
  [ConnectionConfiguration](#cfn-kendra-datasource-databaseconfiguration-connectionconfiguration): 
    ConnectionConfiguration
  [DatabaseEngineType](#cfn-kendra-datasource-databaseconfiguration-databaseenginetype): String
  [SqlConfiguration](#cfn-kendra-datasource-databaseconfiguration-sqlconfiguration): 
    SqlConfiguration
  [VpcConfiguration](#cfn-kendra-datasource-databaseconfiguration-vpcconfiguration): 
    DataSourceVpcConfiguration
```

## Properties<a name="aws-properties-kendra-datasource-databaseconfiguration-properties"></a>

`AclConfiguration`  <a name="cfn-kendra-datasource-databaseconfiguration-aclconfiguration"></a>
Information about the database column that provides information for user context filtering\.  
*Required*: No  
*Type*: [AclConfiguration](aws-properties-kendra-datasource-aclconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnConfiguration`  <a name="cfn-kendra-datasource-databaseconfiguration-columnconfiguration"></a>
Information about where the index should get the document information from the database\.  
*Required*: Yes  
*Type*: [ColumnConfiguration](aws-properties-kendra-datasource-columnconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionConfiguration`  <a name="cfn-kendra-datasource-databaseconfiguration-connectionconfiguration"></a>
The information necessary to connect to a database\.  
*Required*: Yes  
*Type*: [ConnectionConfiguration](aws-properties-kendra-datasource-connectionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseEngineType`  <a name="cfn-kendra-datasource-databaseconfiguration-databaseenginetype"></a>
The type of database engine that runs the database\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `RDS_AURORA_MYSQL | RDS_AURORA_POSTGRESQL | RDS_MYSQL | RDS_POSTGRESQL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqlConfiguration`  <a name="cfn-kendra-datasource-databaseconfiguration-sqlconfiguration"></a>
Provides information about how Amazon Kendra uses quote marks around SQL identifiers when querying a database data source\.  
*Required*: No  
*Type*: [SqlConfiguration](aws-properties-kendra-datasource-sqlconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfiguration`  <a name="cfn-kendra-datasource-databaseconfiguration-vpcconfiguration"></a>
Provides information for connecting to an Amazon VPC\.  
*Required*: No  
*Type*: [DataSourceVpcConfiguration](aws-properties-kendra-datasource-datasourcevpcconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)