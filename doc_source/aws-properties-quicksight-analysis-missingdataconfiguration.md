# AWS::QuickSight::Analysis MissingDataConfiguration<a name="aws-properties-quicksight-analysis-missingdataconfiguration"></a>

The configuration options that determine how missing data is treated during the rendering of a line chart\.

## Syntax<a name="aws-properties-quicksight-analysis-missingdataconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-missingdataconfiguration-syntax.json"></a>

```
{
  "[TreatmentOption](#cfn-quicksight-analysis-missingdataconfiguration-treatmentoption)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-missingdataconfiguration-syntax.yaml"></a>

```
  [TreatmentOption](#cfn-quicksight-analysis-missingdataconfiguration-treatmentoption): String
```

## Properties<a name="aws-properties-quicksight-analysis-missingdataconfiguration-properties"></a>

`TreatmentOption`  <a name="cfn-quicksight-analysis-missingdataconfiguration-treatmentoption"></a>
The treatment option that determines how missing data should be rendered\. Choose from the following options:  
+  `INTERPOLATE`: Interpolate missing values between the prior and the next known value\.
+  `SHOW_AS_ZERO`: Show missing values as the value `0`\.
+  `SHOW_AS_BLANK`: Display a blank space when rendering missing data\.
*Required*: No  
*Type*: String  
*Allowed values*: `INTERPOLATE | SHOW_AS_BLANK | SHOW_AS_ZERO`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)