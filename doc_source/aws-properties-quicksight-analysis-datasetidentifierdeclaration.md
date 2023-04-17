# AWS::QuickSight::Analysis DataSetIdentifierDeclaration<a name="aws-properties-quicksight-analysis-datasetidentifierdeclaration"></a>

A data set\.

## Syntax<a name="aws-properties-quicksight-analysis-datasetidentifierdeclaration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-datasetidentifierdeclaration-syntax.json"></a>

```
{
  "[DataSetArn](#cfn-quicksight-analysis-datasetidentifierdeclaration-datasetarn)" : String,
  "[Identifier](#cfn-quicksight-analysis-datasetidentifierdeclaration-identifier)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-datasetidentifierdeclaration-syntax.yaml"></a>

```
  [DataSetArn](#cfn-quicksight-analysis-datasetidentifierdeclaration-datasetarn): String
  [Identifier](#cfn-quicksight-analysis-datasetidentifierdeclaration-identifier): String
```

## Properties<a name="aws-properties-quicksight-analysis-datasetidentifierdeclaration-properties"></a>

`DataSetArn`  <a name="cfn-quicksight-analysis-datasetidentifierdeclaration-datasetarn"></a>
The Amazon Resource Name \(ARN\) of the data set\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Identifier`  <a name="cfn-quicksight-analysis-datasetidentifierdeclaration-identifier"></a>
The identifier of the data set, typically the data set's name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)