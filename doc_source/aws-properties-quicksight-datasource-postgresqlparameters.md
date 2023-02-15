# AWS::QuickSight::DataSource PostgreSqlParameters<a name="aws-properties-quicksight-datasource-postgresqlparameters"></a>

The parameters for PostgreSQL\.

## Syntax<a name="aws-properties-quicksight-datasource-postgresqlparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-postgresqlparameters-syntax.json"></a>

```
{
  "[Database](#cfn-quicksight-datasource-postgresqlparameters-database)" : String,
  "[Host](#cfn-quicksight-datasource-postgresqlparameters-host)" : String,
  "[Port](#cfn-quicksight-datasource-postgresqlparameters-port)" : Double
}
```

### YAML<a name="aws-properties-quicksight-datasource-postgresqlparameters-syntax.yaml"></a>

```
  [Database](#cfn-quicksight-datasource-postgresqlparameters-database): String
  [Host](#cfn-quicksight-datasource-postgresqlparameters-host): String
  [Port](#cfn-quicksight-datasource-postgresqlparameters-port): Double
```

## Properties<a name="aws-properties-quicksight-datasource-postgresqlparameters-properties"></a>

`Database`  <a name="cfn-quicksight-datasource-postgresqlparameters-database"></a>
Database\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Host`  <a name="cfn-quicksight-datasource-postgresqlparameters-host"></a>
Host\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-quicksight-datasource-postgresqlparameters-port"></a>
Port\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)