# AWS::QuickSight::Topic TopicSingularFilterConstant<a name="aws-properties-quicksight-topic-topicsingularfilterconstant"></a>

A structure that represents a singular filter constant, used in filters to specify a single value to match against\.

## Syntax<a name="aws-properties-quicksight-topic-topicsingularfilterconstant-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-topicsingularfilterconstant-syntax.json"></a>

```
{
  "[ConstantType](#cfn-quicksight-topic-topicsingularfilterconstant-constanttype)" : String,
  "[SingularConstant](#cfn-quicksight-topic-topicsingularfilterconstant-singularconstant)" : String
}
```

### YAML<a name="aws-properties-quicksight-topic-topicsingularfilterconstant-syntax.yaml"></a>

```
  [ConstantType](#cfn-quicksight-topic-topicsingularfilterconstant-constanttype): String
  [SingularConstant](#cfn-quicksight-topic-topicsingularfilterconstant-singularconstant): String
```

## Properties<a name="aws-properties-quicksight-topic-topicsingularfilterconstant-properties"></a>

`ConstantType`  <a name="cfn-quicksight-topic-topicsingularfilterconstant-constanttype"></a>
The type of the singular filter constant\. Valid values for this structure are `SINGULAR`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `COLLECTIVE | RANGE | SINGULAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingularConstant`  <a name="cfn-quicksight-topic-topicsingularfilterconstant-singularconstant"></a>
The value of the singular filter constant\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)