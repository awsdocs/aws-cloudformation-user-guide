# AWS::QuickSight::DataSource DatabricksParameters<a name="aws-properties-quicksight-datasource-databricksparameters"></a>

The required parameters that are needed to connect to a Databricks data source\.

## Syntax<a name="aws-properties-quicksight-datasource-databricksparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-databricksparameters-syntax.json"></a>

```
{
  "[Host](#cfn-quicksight-datasource-databricksparameters-host)" : String,
  "[Port](#cfn-quicksight-datasource-databricksparameters-port)" : Double,
  "[SqlEndpointPath](#cfn-quicksight-datasource-databricksparameters-sqlendpointpath)" : String
}
```

### YAML<a name="aws-properties-quicksight-datasource-databricksparameters-syntax.yaml"></a>

```
  [Host](#cfn-quicksight-datasource-databricksparameters-host): String
  [Port](#cfn-quicksight-datasource-databricksparameters-port): Double
  [SqlEndpointPath](#cfn-quicksight-datasource-databricksparameters-sqlendpointpath): String
```

## Properties<a name="aws-properties-quicksight-datasource-databricksparameters-properties"></a>

`Host`  <a name="cfn-quicksight-datasource-databricksparameters-host"></a>
The host name of the Databricks data source\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-quicksight-datasource-databricksparameters-port"></a>
The port for the Databricks data source\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqlEndpointPath`  <a name="cfn-quicksight-datasource-databricksparameters-sqlendpointpath"></a>
The HTTP path of the Databricks data source\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)