# AWS::QuickSight::Template StringValueWhenUnsetConfiguration<a name="aws-properties-quicksight-template-stringvaluewhenunsetconfiguration"></a>

The configuration that defines the default value of a `String` parameter when a value has not been set\.

## Syntax<a name="aws-properties-quicksight-template-stringvaluewhenunsetconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-stringvaluewhenunsetconfiguration-syntax.json"></a>

```
{
  "[CustomValue](#cfn-quicksight-template-stringvaluewhenunsetconfiguration-customvalue)" : String,
  "[ValueWhenUnsetOption](#cfn-quicksight-template-stringvaluewhenunsetconfiguration-valuewhenunsetoption)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-stringvaluewhenunsetconfiguration-syntax.yaml"></a>

```
  [CustomValue](#cfn-quicksight-template-stringvaluewhenunsetconfiguration-customvalue): String
  [ValueWhenUnsetOption](#cfn-quicksight-template-stringvaluewhenunsetconfiguration-valuewhenunsetoption): String
```

## Properties<a name="aws-properties-quicksight-template-stringvaluewhenunsetconfiguration-properties"></a>

`CustomValue`  <a name="cfn-quicksight-template-stringvaluewhenunsetconfiguration-customvalue"></a>
A custom value that's used when the value of a parameter isn't set\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueWhenUnsetOption`  <a name="cfn-quicksight-template-stringvaluewhenunsetconfiguration-valuewhenunsetoption"></a>
The built\-in options for default values\. The value can be one of the following:  
+  `RECOMMENDED`: The recommended value\.
+  `NULL`: The `NULL` value\.
*Required*: No  
*Type*: String  
*Allowed values*: `NULL | RECOMMENDED_VALUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)