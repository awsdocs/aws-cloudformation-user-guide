# AWS::QuickSight::Analysis AnchorDateConfiguration<a name="aws-properties-quicksight-analysis-anchordateconfiguration"></a>

The date configuration of the filter\.

## Syntax<a name="aws-properties-quicksight-analysis-anchordateconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-anchordateconfiguration-syntax.json"></a>

```
{
  "[AnchorOption](#cfn-quicksight-analysis-anchordateconfiguration-anchoroption)" : String,
  "[ParameterName](#cfn-quicksight-analysis-anchordateconfiguration-parametername)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-anchordateconfiguration-syntax.yaml"></a>

```
  [AnchorOption](#cfn-quicksight-analysis-anchordateconfiguration-anchoroption): String
  [ParameterName](#cfn-quicksight-analysis-anchordateconfiguration-parametername): String
```

## Properties<a name="aws-properties-quicksight-analysis-anchordateconfiguration-properties"></a>

`AnchorOption`  <a name="cfn-quicksight-analysis-anchordateconfiguration-anchoroption"></a>
The options for the date configuration\. Choose one of the options below:  
+  `NOW` 
*Required*: No  
*Type*: String  
*Allowed values*: `NOW`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterName`  <a name="cfn-quicksight-analysis-anchordateconfiguration-parametername"></a>
The name of the parameter that is used for the anchor date configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)