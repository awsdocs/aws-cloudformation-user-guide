# AWS::QuickSight::DataSource AuroraParameters<a name="aws-properties-quicksight-datasource-auroraparameters"></a>

Parameters for Amazon Aurora\.

## Syntax<a name="aws-properties-quicksight-datasource-auroraparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-auroraparameters-syntax.json"></a>

```
{
  "[Database](#cfn-quicksight-datasource-auroraparameters-database)" : String,
  "[Host](#cfn-quicksight-datasource-auroraparameters-host)" : String,
  "[Port](#cfn-quicksight-datasource-auroraparameters-port)" : Double
}
```

### YAML<a name="aws-properties-quicksight-datasource-auroraparameters-syntax.yaml"></a>

```
  [Database](#cfn-quicksight-datasource-auroraparameters-database): String
  [Host](#cfn-quicksight-datasource-auroraparameters-host): String
  [Port](#cfn-quicksight-datasource-auroraparameters-port): Double
```

## Properties<a name="aws-properties-quicksight-datasource-auroraparameters-properties"></a>

`Database`  <a name="cfn-quicksight-datasource-auroraparameters-database"></a>
Database\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Host`  <a name="cfn-quicksight-datasource-auroraparameters-host"></a>
Host\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-quicksight-datasource-auroraparameters-port"></a>
Port\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)