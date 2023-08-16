# AWS::QuickSight::Topic TopicRangeFilterConstant<a name="aws-properties-quicksight-topic-topicrangefilterconstant"></a>

A constant value that is used in a range filter to specify the endpoints of the range\.

## Syntax<a name="aws-properties-quicksight-topic-topicrangefilterconstant-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-topicrangefilterconstant-syntax.json"></a>

```
{
  "[ConstantType](#cfn-quicksight-topic-topicrangefilterconstant-constanttype)" : String,
  "[RangeConstant](#cfn-quicksight-topic-topicrangefilterconstant-rangeconstant)" : RangeConstant
}
```

### YAML<a name="aws-properties-quicksight-topic-topicrangefilterconstant-syntax.yaml"></a>

```
  [ConstantType](#cfn-quicksight-topic-topicrangefilterconstant-constanttype): String
  [RangeConstant](#cfn-quicksight-topic-topicrangefilterconstant-rangeconstant): 
    RangeConstant
```

## Properties<a name="aws-properties-quicksight-topic-topicrangefilterconstant-properties"></a>

`ConstantType`  <a name="cfn-quicksight-topic-topicrangefilterconstant-constanttype"></a>
The data type of the constant value that is used in a range filter\. Valid values for this structure are `RANGE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `COLLECTIVE | RANGE | SINGULAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeConstant`  <a name="cfn-quicksight-topic-topicrangefilterconstant-rangeconstant"></a>
The value of the constant that is used to specify the endpoints of a range filter\.  
*Required*: No  
*Type*: [RangeConstant](aws-properties-quicksight-topic-rangeconstant.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)