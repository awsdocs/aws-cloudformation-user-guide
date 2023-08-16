# AWS::QuickSight::Topic TopicCategoryFilterConstant<a name="aws-properties-quicksight-topic-topiccategoryfilterconstant"></a>

A constant used in a category filter\.

## Syntax<a name="aws-properties-quicksight-topic-topiccategoryfilterconstant-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-topiccategoryfilterconstant-syntax.json"></a>

```
{
  "[CollectiveConstant](#cfn-quicksight-topic-topiccategoryfilterconstant-collectiveconstant)" : CollectiveConstant,
  "[ConstantType](#cfn-quicksight-topic-topiccategoryfilterconstant-constanttype)" : String,
  "[SingularConstant](#cfn-quicksight-topic-topiccategoryfilterconstant-singularconstant)" : String
}
```

### YAML<a name="aws-properties-quicksight-topic-topiccategoryfilterconstant-syntax.yaml"></a>

```
  [CollectiveConstant](#cfn-quicksight-topic-topiccategoryfilterconstant-collectiveconstant): 
    CollectiveConstant
  [ConstantType](#cfn-quicksight-topic-topiccategoryfilterconstant-constanttype): String
  [SingularConstant](#cfn-quicksight-topic-topiccategoryfilterconstant-singularconstant): String
```

## Properties<a name="aws-properties-quicksight-topic-topiccategoryfilterconstant-properties"></a>

`CollectiveConstant`  <a name="cfn-quicksight-topic-topiccategoryfilterconstant-collectiveconstant"></a>
A collective constant used in a category filter\. This element is used to specify a list of values for the constant\.  
*Required*: No  
*Type*: [CollectiveConstant](aws-properties-quicksight-topic-collectiveconstant.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConstantType`  <a name="cfn-quicksight-topic-topiccategoryfilterconstant-constanttype"></a>
The type of category filter constant\. This element is used to specify whether a constant is a singular or collective\. Valid values are `SINGULAR` and `COLLECTIVE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `COLLECTIVE | RANGE | SINGULAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingularConstant`  <a name="cfn-quicksight-topic-topiccategoryfilterconstant-singularconstant"></a>
A singular constant used in a category filter\. This element is used to specify a single value for the constant\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)