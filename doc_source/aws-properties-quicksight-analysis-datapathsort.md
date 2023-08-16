# AWS::QuickSight::Analysis DataPathSort<a name="aws-properties-quicksight-analysis-datapathsort"></a>

Allows data paths to be sorted by a specific data value\.

## Syntax<a name="aws-properties-quicksight-analysis-datapathsort-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-datapathsort-syntax.json"></a>

```
{
  "[Direction](#cfn-quicksight-analysis-datapathsort-direction)" : String,
  "[SortPaths](#cfn-quicksight-analysis-datapathsort-sortpaths)" : [ DataPathValue, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-datapathsort-syntax.yaml"></a>

```
  [Direction](#cfn-quicksight-analysis-datapathsort-direction): String
  [SortPaths](#cfn-quicksight-analysis-datapathsort-sortpaths): 
    - DataPathValue
```

## Properties<a name="aws-properties-quicksight-analysis-datapathsort-properties"></a>

`Direction`  <a name="cfn-quicksight-analysis-datapathsort-direction"></a>
Determines the sort direction\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ASC | DESC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortPaths`  <a name="cfn-quicksight-analysis-datapathsort-sortpaths"></a>
The list of data paths that need to be sorted\.  
*Required*: Yes  
*Type*: List of [DataPathValue](aws-properties-quicksight-analysis-datapathvalue.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)