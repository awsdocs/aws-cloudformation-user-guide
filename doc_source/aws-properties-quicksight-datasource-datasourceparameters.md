# AWS::QuickSight::DataSource DataSourceParameters<a name="aws-properties-quicksight-datasource-datasourceparameters"></a>

The parameters that Amazon QuickSight uses to connect to your underlying data source\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.

## Syntax<a name="aws-properties-quicksight-datasource-datasourceparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-datasourceparameters-syntax.json"></a>

```
{
  "[AmazonElasticsearchParameters](#cfn-quicksight-datasource-datasourceparameters-amazonelasticsearchparameters)" : AmazonElasticsearchParameters,
  "[AmazonOpenSearchParameters](#cfn-quicksight-datasource-datasourceparameters-amazonopensearchparameters)" : AmazonOpenSearchParameters,
  "[AthenaParameters](#cfn-quicksight-datasource-datasourceparameters-athenaparameters)" : AthenaParameters,
  "[AuroraParameters](#cfn-quicksight-datasource-datasourceparameters-auroraparameters)" : AuroraParameters,
  "[AuroraPostgreSqlParameters](#cfn-quicksight-datasource-datasourceparameters-aurorapostgresqlparameters)" : AuroraPostgreSqlParameters,
  "[DatabricksParameters](#cfn-quicksight-datasource-datasourceparameters-databricksparameters)" : DatabricksParameters,
  "[MariaDbParameters](#cfn-quicksight-datasource-datasourceparameters-mariadbparameters)" : MariaDbParameters,
  "[MySqlParameters](#cfn-quicksight-datasource-datasourceparameters-mysqlparameters)" : MySqlParameters,
  "[OracleParameters](#cfn-quicksight-datasource-datasourceparameters-oracleparameters)" : OracleParameters,
  "[PostgreSqlParameters](#cfn-quicksight-datasource-datasourceparameters-postgresqlparameters)" : PostgreSqlParameters,
  "[PrestoParameters](#cfn-quicksight-datasource-datasourceparameters-prestoparameters)" : PrestoParameters,
  "[RdsParameters](#cfn-quicksight-datasource-datasourceparameters-rdsparameters)" : RdsParameters,
  "[RedshiftParameters](#cfn-quicksight-datasource-datasourceparameters-redshiftparameters)" : RedshiftParameters,
  "[S3Parameters](#cfn-quicksight-datasource-datasourceparameters-s3parameters)" : S3Parameters,
  "[SnowflakeParameters](#cfn-quicksight-datasource-datasourceparameters-snowflakeparameters)" : SnowflakeParameters,
  "[SparkParameters](#cfn-quicksight-datasource-datasourceparameters-sparkparameters)" : SparkParameters,
  "[SqlServerParameters](#cfn-quicksight-datasource-datasourceparameters-sqlserverparameters)" : SqlServerParameters,
  "[TeradataParameters](#cfn-quicksight-datasource-datasourceparameters-teradataparameters)" : TeradataParameters
}
```

### YAML<a name="aws-properties-quicksight-datasource-datasourceparameters-syntax.yaml"></a>

```
  [AmazonElasticsearchParameters](#cfn-quicksight-datasource-datasourceparameters-amazonelasticsearchparameters): 
    AmazonElasticsearchParameters
  [AmazonOpenSearchParameters](#cfn-quicksight-datasource-datasourceparameters-amazonopensearchparameters): 
    AmazonOpenSearchParameters
  [AthenaParameters](#cfn-quicksight-datasource-datasourceparameters-athenaparameters): 
    AthenaParameters
  [AuroraParameters](#cfn-quicksight-datasource-datasourceparameters-auroraparameters): 
    AuroraParameters
  [AuroraPostgreSqlParameters](#cfn-quicksight-datasource-datasourceparameters-aurorapostgresqlparameters): 
    AuroraPostgreSqlParameters
  [DatabricksParameters](#cfn-quicksight-datasource-datasourceparameters-databricksparameters): 
    DatabricksParameters
  [MariaDbParameters](#cfn-quicksight-datasource-datasourceparameters-mariadbparameters): 
    MariaDbParameters
  [MySqlParameters](#cfn-quicksight-datasource-datasourceparameters-mysqlparameters): 
    MySqlParameters
  [OracleParameters](#cfn-quicksight-datasource-datasourceparameters-oracleparameters): 
    OracleParameters
  [PostgreSqlParameters](#cfn-quicksight-datasource-datasourceparameters-postgresqlparameters): 
    PostgreSqlParameters
  [PrestoParameters](#cfn-quicksight-datasource-datasourceparameters-prestoparameters): 
    PrestoParameters
  [RdsParameters](#cfn-quicksight-datasource-datasourceparameters-rdsparameters): 
    RdsParameters
  [RedshiftParameters](#cfn-quicksight-datasource-datasourceparameters-redshiftparameters): 
    RedshiftParameters
  [S3Parameters](#cfn-quicksight-datasource-datasourceparameters-s3parameters): 
    S3Parameters
  [SnowflakeParameters](#cfn-quicksight-datasource-datasourceparameters-snowflakeparameters): 
    SnowflakeParameters
  [SparkParameters](#cfn-quicksight-datasource-datasourceparameters-sparkparameters): 
    SparkParameters
  [SqlServerParameters](#cfn-quicksight-datasource-datasourceparameters-sqlserverparameters): 
    SqlServerParameters
  [TeradataParameters](#cfn-quicksight-datasource-datasourceparameters-teradataparameters): 
    TeradataParameters
```

## Properties<a name="aws-properties-quicksight-datasource-datasourceparameters-properties"></a>

`AmazonElasticsearchParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-amazonelasticsearchparameters"></a>
The parameters for OpenSearch\.  
*Required*: No  
*Type*: [AmazonElasticsearchParameters](aws-properties-quicksight-datasource-amazonelasticsearchparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AmazonOpenSearchParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-amazonopensearchparameters"></a>
The parameters for OpenSearch\.  
*Required*: No  
*Type*: [AmazonOpenSearchParameters](aws-properties-quicksight-datasource-amazonopensearchparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AthenaParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-athenaparameters"></a>
The parameters for Amazon Athena\.  
*Required*: No  
*Type*: [AthenaParameters](aws-properties-quicksight-datasource-athenaparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuroraParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-auroraparameters"></a>
The parameters for Amazon Aurora MySQL\.  
*Required*: No  
*Type*: [AuroraParameters](aws-properties-quicksight-datasource-auroraparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuroraPostgreSqlParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-aurorapostgresqlparameters"></a>
The parameters for Amazon Aurora\.  
*Required*: No  
*Type*: [AuroraPostgreSqlParameters](aws-properties-quicksight-datasource-aurorapostgresqlparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabricksParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-databricksparameters"></a>
Property description not available\.  
*Required*: No  
*Type*: [DatabricksParameters](aws-properties-quicksight-datasource-databricksparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MariaDbParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-mariadbparameters"></a>
The parameters for MariaDB\.  
*Required*: No  
*Type*: [MariaDbParameters](aws-properties-quicksight-datasource-mariadbparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MySqlParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-mysqlparameters"></a>
The parameters for MySQL\.  
*Required*: No  
*Type*: [MySqlParameters](aws-properties-quicksight-datasource-mysqlparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OracleParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-oracleparameters"></a>
Oracle parameters\.  
*Required*: No  
*Type*: [OracleParameters](aws-properties-quicksight-datasource-oracleparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PostgreSqlParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-postgresqlparameters"></a>
The parameters for PostgreSQL\.  
*Required*: No  
*Type*: [PostgreSqlParameters](aws-properties-quicksight-datasource-postgresqlparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrestoParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-prestoparameters"></a>
The parameters for Presto\.  
*Required*: No  
*Type*: [PrestoParameters](aws-properties-quicksight-datasource-prestoparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RdsParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-rdsparameters"></a>
The parameters for Amazon RDS\.  
*Required*: No  
*Type*: [RdsParameters](aws-properties-quicksight-datasource-rdsparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedshiftParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-redshiftparameters"></a>
The parameters for Amazon Redshift\.  
*Required*: No  
*Type*: [RedshiftParameters](aws-properties-quicksight-datasource-redshiftparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Parameters`  <a name="cfn-quicksight-datasource-datasourceparameters-s3parameters"></a>
The parameters for S3\.  
*Required*: No  
*Type*: [S3Parameters](aws-properties-quicksight-datasource-s3parameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnowflakeParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-snowflakeparameters"></a>
The parameters for Snowflake\.  
*Required*: No  
*Type*: [SnowflakeParameters](aws-properties-quicksight-datasource-snowflakeparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SparkParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-sparkparameters"></a>
The parameters for Spark\.  
*Required*: No  
*Type*: [SparkParameters](aws-properties-quicksight-datasource-sparkparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqlServerParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-sqlserverparameters"></a>
The parameters for SQL Server\.  
*Required*: No  
*Type*: [SqlServerParameters](aws-properties-quicksight-datasource-sqlserverparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TeradataParameters`  <a name="cfn-quicksight-datasource-datasourceparameters-teradataparameters"></a>
The parameters for Teradata\.  
*Required*: No  
*Type*: [TeradataParameters](aws-properties-quicksight-datasource-teradataparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)