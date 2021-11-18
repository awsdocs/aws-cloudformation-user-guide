# AWS::QuickSight::DataSource MySqlParameters<a name="aws-properties-quicksight-datasource-mysqlparameters"></a>

The parameters for MySQL\.

## Syntax<a name="aws-properties-quicksight-datasource-mysqlparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-mysqlparameters-syntax.json"></a>

```
{
  "[Database](#cfn-quicksight-datasource-mysqlparameters-database)" : String,
  "[Host](#cfn-quicksight-datasource-mysqlparameters-host)" : String,
  "[Port](#cfn-quicksight-datasource-mysqlparameters-port)" : Double
}
```

### YAML<a name="aws-properties-quicksight-datasource-mysqlparameters-syntax.yaml"></a>

```
  [Database](#cfn-quicksight-datasource-mysqlparameters-database): String
  [Host](#cfn-quicksight-datasource-mysqlparameters-host): String
  [Port](#cfn-quicksight-datasource-mysqlparameters-port): Double
```

## Properties<a name="aws-properties-quicksight-datasource-mysqlparameters-properties"></a>

`Database`  <a name="cfn-quicksight-datasource-mysqlparameters-database"></a>
Database\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Host`  <a name="cfn-quicksight-datasource-mysqlparameters-host"></a>
Host\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-quicksight-datasource-mysqlparameters-port"></a>
Port\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)