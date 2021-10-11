# AWS::QuickSight::DataSource AuroraPostgreSqlParameters<a name="aws-properties-quicksight-datasource-aurorapostgresqlparameters"></a>

Parameters for Amazon Aurora PostgreSQL\-Compatible Edition\.

## Syntax<a name="aws-properties-quicksight-datasource-aurorapostgresqlparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-aurorapostgresqlparameters-syntax.json"></a>

```
{
  "[Database](#cfn-quicksight-datasource-aurorapostgresqlparameters-database)" : String,
  "[Host](#cfn-quicksight-datasource-aurorapostgresqlparameters-host)" : String,
  "[Port](#cfn-quicksight-datasource-aurorapostgresqlparameters-port)" : Double
}
```

### YAML<a name="aws-properties-quicksight-datasource-aurorapostgresqlparameters-syntax.yaml"></a>

```
  [Database](#cfn-quicksight-datasource-aurorapostgresqlparameters-database): String
  [Host](#cfn-quicksight-datasource-aurorapostgresqlparameters-host): String
  [Port](#cfn-quicksight-datasource-aurorapostgresqlparameters-port): Double
```

## Properties<a name="aws-properties-quicksight-datasource-aurorapostgresqlparameters-properties"></a>

`Database`  <a name="cfn-quicksight-datasource-aurorapostgresqlparameters-database"></a>
The Amazon Aurora PostgreSQL database to connect to\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Host`  <a name="cfn-quicksight-datasource-aurorapostgresqlparameters-host"></a>
The Amazon Aurora PostgreSQL\-Compatible host to connect to\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-quicksight-datasource-aurorapostgresqlparameters-port"></a>
The port that Amazon Aurora PostgreSQL is listening on\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)