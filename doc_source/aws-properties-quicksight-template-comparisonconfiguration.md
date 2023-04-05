# AWS::QuickSight::Template ComparisonConfiguration<a name="aws-properties-quicksight-template-comparisonconfiguration"></a>

The comparison display configuration of a KPI or gauge chart\.

## Syntax<a name="aws-properties-quicksight-template-comparisonconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-comparisonconfiguration-syntax.json"></a>

```
{
  "[ComparisonFormat](#cfn-quicksight-template-comparisonconfiguration-comparisonformat)" : ComparisonFormatConfiguration,
  "[ComparisonMethod](#cfn-quicksight-template-comparisonconfiguration-comparisonmethod)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-comparisonconfiguration-syntax.yaml"></a>

```
  [ComparisonFormat](#cfn-quicksight-template-comparisonconfiguration-comparisonformat): 
    ComparisonFormatConfiguration
  [ComparisonMethod](#cfn-quicksight-template-comparisonconfiguration-comparisonmethod): String
```

## Properties<a name="aws-properties-quicksight-template-comparisonconfiguration-properties"></a>

`ComparisonFormat`  <a name="cfn-quicksight-template-comparisonconfiguration-comparisonformat"></a>
The format of the comparison\.  
*Required*: No  
*Type*: [ComparisonFormatConfiguration](aws-properties-quicksight-template-comparisonformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComparisonMethod`  <a name="cfn-quicksight-template-comparisonconfiguration-comparisonmethod"></a>
The method of the comparison\. Choose from the following options:  
+  `DIFFERENCE` 
+  `PERCENT_DIFFERENCE` 
+  `PERCENT` 
*Required*: No  
*Type*: String  
*Allowed values*: `DIFFERENCE | PERCENT | PERCENT_DIFFERENCE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)