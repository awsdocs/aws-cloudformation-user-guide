# AWS::QuickSight::Template TemplateSourceAnalysis<a name="aws-properties-quicksight-template-templatesourceanalysis"></a>

The source analysis of the template\.

## Syntax<a name="aws-properties-quicksight-template-templatesourceanalysis-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-templatesourceanalysis-syntax.json"></a>

```
{
  "[Arn](#cfn-quicksight-template-templatesourceanalysis-arn)" : String,
  "[DataSetReferences](#cfn-quicksight-template-templatesourceanalysis-datasetreferences)" : [ DataSetReference, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-templatesourceanalysis-syntax.yaml"></a>

```
  [Arn](#cfn-quicksight-template-templatesourceanalysis-arn): String
  [DataSetReferences](#cfn-quicksight-template-templatesourceanalysis-datasetreferences): 
    - DataSetReference
```

## Properties<a name="aws-properties-quicksight-template-templatesourceanalysis-properties"></a>

`Arn`  <a name="cfn-quicksight-template-templatesourceanalysis-arn"></a>
The Amazon Resource Name \(ARN\) of the resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSetReferences`  <a name="cfn-quicksight-template-templatesourceanalysis-datasetreferences"></a>
A structure containing information about the dataset references used as placeholders in the template\.  
*Required*: Yes  
*Type*: List of [DataSetReference](aws-properties-quicksight-template-datasetreference.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)