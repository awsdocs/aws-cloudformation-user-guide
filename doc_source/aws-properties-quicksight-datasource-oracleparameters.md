# AWS::QuickSight::DataSource OracleParameters<a name="aws-properties-quicksight-datasource-oracleparameters"></a>

Oracle parameters\.

## Syntax<a name="aws-properties-quicksight-datasource-oracleparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-oracleparameters-syntax.json"></a>

```
{
  "[Database](#cfn-quicksight-datasource-oracleparameters-database)" : String,
  "[Host](#cfn-quicksight-datasource-oracleparameters-host)" : String,
  "[Port](#cfn-quicksight-datasource-oracleparameters-port)" : Double
}
```

### YAML<a name="aws-properties-quicksight-datasource-oracleparameters-syntax.yaml"></a>

```
  [Database](#cfn-quicksight-datasource-oracleparameters-database): String
  [Host](#cfn-quicksight-datasource-oracleparameters-host): String
  [Port](#cfn-quicksight-datasource-oracleparameters-port): Double
```

## Properties<a name="aws-properties-quicksight-datasource-oracleparameters-properties"></a>

`Database`  <a name="cfn-quicksight-datasource-oracleparameters-database"></a>
Database\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Host`  <a name="cfn-quicksight-datasource-oracleparameters-host"></a>
Host\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-quicksight-datasource-oracleparameters-port"></a>
Port\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)