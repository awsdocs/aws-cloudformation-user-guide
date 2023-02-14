# AWS::QuickSight::DataSource SnowflakeParameters<a name="aws-properties-quicksight-datasource-snowflakeparameters"></a>

The parameters for Snowflake\.

## Syntax<a name="aws-properties-quicksight-datasource-snowflakeparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-snowflakeparameters-syntax.json"></a>

```
{
  "[Database](#cfn-quicksight-datasource-snowflakeparameters-database)" : String,
  "[Host](#cfn-quicksight-datasource-snowflakeparameters-host)" : String,
  "[Warehouse](#cfn-quicksight-datasource-snowflakeparameters-warehouse)" : String
}
```

### YAML<a name="aws-properties-quicksight-datasource-snowflakeparameters-syntax.yaml"></a>

```
  [Database](#cfn-quicksight-datasource-snowflakeparameters-database): String
  [Host](#cfn-quicksight-datasource-snowflakeparameters-host): String
  [Warehouse](#cfn-quicksight-datasource-snowflakeparameters-warehouse): String
```

## Properties<a name="aws-properties-quicksight-datasource-snowflakeparameters-properties"></a>

`Database`  <a name="cfn-quicksight-datasource-snowflakeparameters-database"></a>
Database\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Host`  <a name="cfn-quicksight-datasource-snowflakeparameters-host"></a>
Host\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Warehouse`  <a name="cfn-quicksight-datasource-snowflakeparameters-warehouse"></a>
Warehouse\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)