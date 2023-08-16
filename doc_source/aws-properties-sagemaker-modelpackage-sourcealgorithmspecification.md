# AWS::SageMaker::ModelPackage SourceAlgorithmSpecification<a name="aws-properties-sagemaker-modelpackage-sourcealgorithmspecification"></a>

A list of algorithms that were used to create a model package\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-sourcealgorithmspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-sourcealgorithmspecification-syntax.json"></a>

```
{
  "[SourceAlgorithms](#cfn-sagemaker-modelpackage-sourcealgorithmspecification-sourcealgorithms)" : [ SourceAlgorithm, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-sourcealgorithmspecification-syntax.yaml"></a>

```
  [SourceAlgorithms](#cfn-sagemaker-modelpackage-sourcealgorithmspecification-sourcealgorithms): 
    - SourceAlgorithm
```

## Properties<a name="aws-properties-sagemaker-modelpackage-sourcealgorithmspecification-properties"></a>

`SourceAlgorithms`  <a name="cfn-sagemaker-modelpackage-sourcealgorithmspecification-sourcealgorithms"></a>
A list of the algorithms that were used to create a model package\.  
*Required*: Yes  
*Type*: List of [SourceAlgorithm](aws-properties-sagemaker-modelpackage-sourcealgorithm.md)  
*Maximum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)