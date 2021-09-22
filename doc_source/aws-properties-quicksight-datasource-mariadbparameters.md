# AWS::QuickSight::DataSource MariaDbParameters<a name="aws-properties-quicksight-datasource-mariadbparameters"></a>

The parameters for MariaDB\.

## Syntax<a name="aws-properties-quicksight-datasource-mariadbparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-mariadbparameters-syntax.json"></a>

```
{
  "[Database](#cfn-quicksight-datasource-mariadbparameters-database)" : String,
  "[Host](#cfn-quicksight-datasource-mariadbparameters-host)" : String,
  "[Port](#cfn-quicksight-datasource-mariadbparameters-port)" : Double
}
```

### YAML<a name="aws-properties-quicksight-datasource-mariadbparameters-syntax.yaml"></a>

```
  [Database](#cfn-quicksight-datasource-mariadbparameters-database): String
  [Host](#cfn-quicksight-datasource-mariadbparameters-host): String
  [Port](#cfn-quicksight-datasource-mariadbparameters-port): Double
```

## Properties<a name="aws-properties-quicksight-datasource-mariadbparameters-properties"></a>

`Database`  <a name="cfn-quicksight-datasource-mariadbparameters-database"></a>
Database\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Host`  <a name="cfn-quicksight-datasource-mariadbparameters-host"></a>
Host\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-quicksight-datasource-mariadbparameters-port"></a>
Port\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)