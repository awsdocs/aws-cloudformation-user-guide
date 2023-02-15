# AWS::QuickSight::DataSource SqlServerParameters<a name="aws-properties-quicksight-datasource-sqlserverparameters"></a>

The parameters for SQL Server\.

## Syntax<a name="aws-properties-quicksight-datasource-sqlserverparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-sqlserverparameters-syntax.json"></a>

```
{
  "[Database](#cfn-quicksight-datasource-sqlserverparameters-database)" : String,
  "[Host](#cfn-quicksight-datasource-sqlserverparameters-host)" : String,
  "[Port](#cfn-quicksight-datasource-sqlserverparameters-port)" : Double
}
```

### YAML<a name="aws-properties-quicksight-datasource-sqlserverparameters-syntax.yaml"></a>

```
  [Database](#cfn-quicksight-datasource-sqlserverparameters-database): String
  [Host](#cfn-quicksight-datasource-sqlserverparameters-host): String
  [Port](#cfn-quicksight-datasource-sqlserverparameters-port): Double
```

## Properties<a name="aws-properties-quicksight-datasource-sqlserverparameters-properties"></a>

`Database`  <a name="cfn-quicksight-datasource-sqlserverparameters-database"></a>
Database\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Host`  <a name="cfn-quicksight-datasource-sqlserverparameters-host"></a>
Host\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-quicksight-datasource-sqlserverparameters-port"></a>
Port\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)