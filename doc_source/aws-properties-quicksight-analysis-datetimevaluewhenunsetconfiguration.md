# AWS::QuickSight::Analysis DateTimeValueWhenUnsetConfiguration<a name="aws-properties-quicksight-analysis-datetimevaluewhenunsetconfiguration"></a>

The configuration that defines the default value of a `DateTime` parameter when a value has not been set\.

## Syntax<a name="aws-properties-quicksight-analysis-datetimevaluewhenunsetconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-datetimevaluewhenunsetconfiguration-syntax.json"></a>

```
{
  "[CustomValue](#cfn-quicksight-analysis-datetimevaluewhenunsetconfiguration-customvalue)" : String,
  "[ValueWhenUnsetOption](#cfn-quicksight-analysis-datetimevaluewhenunsetconfiguration-valuewhenunsetoption)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-datetimevaluewhenunsetconfiguration-syntax.yaml"></a>

```
  [CustomValue](#cfn-quicksight-analysis-datetimevaluewhenunsetconfiguration-customvalue): String
  [ValueWhenUnsetOption](#cfn-quicksight-analysis-datetimevaluewhenunsetconfiguration-valuewhenunsetoption): String
```

## Properties<a name="aws-properties-quicksight-analysis-datetimevaluewhenunsetconfiguration-properties"></a>

`CustomValue`  <a name="cfn-quicksight-analysis-datetimevaluewhenunsetconfiguration-customvalue"></a>
A custom value that's used when the value of a parameter isn't set\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueWhenUnsetOption`  <a name="cfn-quicksight-analysis-datetimevaluewhenunsetconfiguration-valuewhenunsetoption"></a>
The built\-in options for default values\. The value can be one of the following:  
+  `RECOMMENDED`: The recommended value\.
+  `NULL`: The `NULL` value\.
*Required*: No  
*Type*: String  
*Allowed values*: `NULL | RECOMMENDED_VALUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)