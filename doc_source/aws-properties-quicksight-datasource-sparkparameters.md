# AWS::QuickSight::DataSource SparkParameters<a name="aws-properties-quicksight-datasource-sparkparameters"></a>

The parameters for Spark\.

## Syntax<a name="aws-properties-quicksight-datasource-sparkparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-sparkparameters-syntax.json"></a>

```
{
  "[Host](#cfn-quicksight-datasource-sparkparameters-host)" : String,
  "[Port](#cfn-quicksight-datasource-sparkparameters-port)" : Double
}
```

### YAML<a name="aws-properties-quicksight-datasource-sparkparameters-syntax.yaml"></a>

```
  [Host](#cfn-quicksight-datasource-sparkparameters-host): String
  [Port](#cfn-quicksight-datasource-sparkparameters-port): Double
```

## Properties<a name="aws-properties-quicksight-datasource-sparkparameters-properties"></a>

`Host`  <a name="cfn-quicksight-datasource-sparkparameters-host"></a>
Host\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-quicksight-datasource-sparkparameters-port"></a>
Port\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)