# AWS::QuickSight::Topic CellValueSynonym<a name="aws-properties-quicksight-topic-cellvaluesynonym"></a>

A structure that represents the cell value synonym\.

## Syntax<a name="aws-properties-quicksight-topic-cellvaluesynonym-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-cellvaluesynonym-syntax.json"></a>

```
{
  "[CellValue](#cfn-quicksight-topic-cellvaluesynonym-cellvalue)" : String,
  "[Synonyms](#cfn-quicksight-topic-cellvaluesynonym-synonyms)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-quicksight-topic-cellvaluesynonym-syntax.yaml"></a>

```
  [CellValue](#cfn-quicksight-topic-cellvaluesynonym-cellvalue): String
  [Synonyms](#cfn-quicksight-topic-cellvaluesynonym-synonyms): 
    - String
```

## Properties<a name="aws-properties-quicksight-topic-cellvaluesynonym-properties"></a>

`CellValue`  <a name="cfn-quicksight-topic-cellvaluesynonym-cellvalue"></a>
The cell value\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Synonyms`  <a name="cfn-quicksight-topic-cellvaluesynonym-synonyms"></a>
Other names or aliases for the cell value\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)