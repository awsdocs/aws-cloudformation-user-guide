# AWS::QuickSight::DataSet JoinInstruction<a name="aws-properties-quicksight-dataset-joininstruction"></a>

The instructions associated with a join\. 

## Syntax<a name="aws-properties-quicksight-dataset-joininstruction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-joininstruction-syntax.json"></a>

```
{
  "[LeftJoinKeyProperties](#cfn-quicksight-dataset-joininstruction-leftjoinkeyproperties)" : JoinKeyProperties,
  "[LeftOperand](#cfn-quicksight-dataset-joininstruction-leftoperand)" : String,
  "[OnClause](#cfn-quicksight-dataset-joininstruction-onclause)" : String,
  "[RightJoinKeyProperties](#cfn-quicksight-dataset-joininstruction-rightjoinkeyproperties)" : JoinKeyProperties,
  "[RightOperand](#cfn-quicksight-dataset-joininstruction-rightoperand)" : String,
  "[Type](#cfn-quicksight-dataset-joininstruction-type)" : String
}
```

### YAML<a name="aws-properties-quicksight-dataset-joininstruction-syntax.yaml"></a>

```
  [LeftJoinKeyProperties](#cfn-quicksight-dataset-joininstruction-leftjoinkeyproperties): 
    JoinKeyProperties
  [LeftOperand](#cfn-quicksight-dataset-joininstruction-leftoperand): String
  [OnClause](#cfn-quicksight-dataset-joininstruction-onclause): String
  [RightJoinKeyProperties](#cfn-quicksight-dataset-joininstruction-rightjoinkeyproperties): 
    JoinKeyProperties
  [RightOperand](#cfn-quicksight-dataset-joininstruction-rightoperand): String
  [Type](#cfn-quicksight-dataset-joininstruction-type): String
```

## Properties<a name="aws-properties-quicksight-dataset-joininstruction-properties"></a>

`LeftJoinKeyProperties`  <a name="cfn-quicksight-dataset-joininstruction-leftjoinkeyproperties"></a>
Join key properties of the left operand\.  
*Required*: No  
*Type*: [JoinKeyProperties](aws-properties-quicksight-dataset-joinkeyproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LeftOperand`  <a name="cfn-quicksight-dataset-joininstruction-leftoperand"></a>
The operand on the left side of a join\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[0-9a-zA-Z-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnClause`  <a name="cfn-quicksight-dataset-joininstruction-onclause"></a>
The join instructions provided in the `ON` clause of a join\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RightJoinKeyProperties`  <a name="cfn-quicksight-dataset-joininstruction-rightjoinkeyproperties"></a>
Join key properties of the right operand\.  
*Required*: No  
*Type*: [JoinKeyProperties](aws-properties-quicksight-dataset-joinkeyproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RightOperand`  <a name="cfn-quicksight-dataset-joininstruction-rightoperand"></a>
The operand on the right side of a join\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[0-9a-zA-Z-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-dataset-joininstruction-type"></a>
The type of join that it is\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `INNER | LEFT | OUTER | RIGHT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)