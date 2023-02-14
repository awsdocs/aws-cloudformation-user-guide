# AWS::QuickSight::DataSet ProjectOperation<a name="aws-properties-quicksight-dataset-projectoperation"></a>

A transform operation that projects columns\. Operations that come after a projection can only refer to projected columns\.

## Syntax<a name="aws-properties-quicksight-dataset-projectoperation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-projectoperation-syntax.json"></a>

```
{
  "[ProjectedColumns](#cfn-quicksight-dataset-projectoperation-projectedcolumns)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dataset-projectoperation-syntax.yaml"></a>

```
  [ProjectedColumns](#cfn-quicksight-dataset-projectoperation-projectedcolumns): 
    - String
```

## Properties<a name="aws-properties-quicksight-dataset-projectoperation-properties"></a>

`ProjectedColumns`  <a name="cfn-quicksight-dataset-projectoperation-projectedcolumns"></a>
Projected columns\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `2000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)