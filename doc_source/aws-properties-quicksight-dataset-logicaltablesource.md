# AWS::QuickSight::DataSet LogicalTableSource<a name="aws-properties-quicksight-dataset-logicaltablesource"></a>

Information about the source of a logical table\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.

## Syntax<a name="aws-properties-quicksight-dataset-logicaltablesource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-logicaltablesource-syntax.json"></a>

```
{
  "[JoinInstruction](#cfn-quicksight-dataset-logicaltablesource-joininstruction)" : JoinInstruction,
  "[PhysicalTableId](#cfn-quicksight-dataset-logicaltablesource-physicaltableid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dataset-logicaltablesource-syntax.yaml"></a>

```
  [JoinInstruction](#cfn-quicksight-dataset-logicaltablesource-joininstruction): 
    JoinInstruction
  [PhysicalTableId](#cfn-quicksight-dataset-logicaltablesource-physicaltableid): String
```

## Properties<a name="aws-properties-quicksight-dataset-logicaltablesource-properties"></a>

`JoinInstruction`  <a name="cfn-quicksight-dataset-logicaltablesource-joininstruction"></a>
Specifies the result of a join of two logical tables\.  
*Required*: No  
*Type*: [JoinInstruction](aws-properties-quicksight-dataset-joininstruction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PhysicalTableId`  <a name="cfn-quicksight-dataset-logicaltablesource-physicaltableid"></a>
Physical table ID\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[0-9a-zA-Z-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)