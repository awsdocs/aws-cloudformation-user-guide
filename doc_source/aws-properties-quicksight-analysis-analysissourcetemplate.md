# AWS::QuickSight::Analysis AnalysisSourceTemplate<a name="aws-properties-quicksight-analysis-analysissourcetemplate"></a>

The source template of an analysis\.

## Syntax<a name="aws-properties-quicksight-analysis-analysissourcetemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-analysissourcetemplate-syntax.json"></a>

```
{
  "[Arn](#cfn-quicksight-analysis-analysissourcetemplate-arn)" : String,
  "[DataSetReferences](#cfn-quicksight-analysis-analysissourcetemplate-datasetreferences)" : [ DataSetReference, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-analysissourcetemplate-syntax.yaml"></a>

```
  [Arn](#cfn-quicksight-analysis-analysissourcetemplate-arn): String
  [DataSetReferences](#cfn-quicksight-analysis-analysissourcetemplate-datasetreferences): 
    - DataSetReference
```

## Properties<a name="aws-properties-quicksight-analysis-analysissourcetemplate-properties"></a>

`Arn`  <a name="cfn-quicksight-analysis-analysissourcetemplate-arn"></a>
The Amazon Resource Name \(ARN\) of the source template of an analysis\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSetReferences`  <a name="cfn-quicksight-analysis-analysissourcetemplate-datasetreferences"></a>
The dataset references of the source template of an analysis\.  
*Required*: Yes  
*Type*: List of [DataSetReference](aws-properties-quicksight-analysis-datasetreference.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)