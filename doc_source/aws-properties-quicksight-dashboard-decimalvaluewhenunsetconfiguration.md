# AWS::QuickSight::Dashboard DecimalValueWhenUnsetConfiguration<a name="aws-properties-quicksight-dashboard-decimalvaluewhenunsetconfiguration"></a>

The configuration that defines the default value of a `Decimal` parameter when a value has not been set\.

## Syntax<a name="aws-properties-quicksight-dashboard-decimalvaluewhenunsetconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-decimalvaluewhenunsetconfiguration-syntax.json"></a>

```
{
  "[CustomValue](#cfn-quicksight-dashboard-decimalvaluewhenunsetconfiguration-customvalue)" : Double,
  "[ValueWhenUnsetOption](#cfn-quicksight-dashboard-decimalvaluewhenunsetconfiguration-valuewhenunsetoption)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-decimalvaluewhenunsetconfiguration-syntax.yaml"></a>

```
  [CustomValue](#cfn-quicksight-dashboard-decimalvaluewhenunsetconfiguration-customvalue): Double
  [ValueWhenUnsetOption](#cfn-quicksight-dashboard-decimalvaluewhenunsetconfiguration-valuewhenunsetoption): String
```

## Properties<a name="aws-properties-quicksight-dashboard-decimalvaluewhenunsetconfiguration-properties"></a>

`CustomValue`  <a name="cfn-quicksight-dashboard-decimalvaluewhenunsetconfiguration-customvalue"></a>
A custom value that's used when the value of a parameter isn't set\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueWhenUnsetOption`  <a name="cfn-quicksight-dashboard-decimalvaluewhenunsetconfiguration-valuewhenunsetoption"></a>
The built\-in options for default values\. The value can be one of the following:  
+  `RECOMMENDED`: The recommended value\.
+  `NULL`: The `NULL` value\.
*Required*: No  
*Type*: String  
*Allowed values*: `NULL | RECOMMENDED_VALUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)