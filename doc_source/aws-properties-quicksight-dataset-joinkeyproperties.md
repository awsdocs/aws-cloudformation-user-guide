# AWS::QuickSight::DataSet JoinKeyProperties<a name="aws-properties-quicksight-dataset-joinkeyproperties"></a>

Properties associated with the columns participating in a join\.

## Syntax<a name="aws-properties-quicksight-dataset-joinkeyproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-joinkeyproperties-syntax.json"></a>

```
{
  "[UniqueKey](#cfn-quicksight-dataset-joinkeyproperties-uniquekey)" : Boolean
}
```

### YAML<a name="aws-properties-quicksight-dataset-joinkeyproperties-syntax.yaml"></a>

```
  [UniqueKey](#cfn-quicksight-dataset-joinkeyproperties-uniquekey): Boolean
```

## Properties<a name="aws-properties-quicksight-dataset-joinkeyproperties-properties"></a>

`UniqueKey`  <a name="cfn-quicksight-dataset-joinkeyproperties-uniquekey"></a>
A value that indicates that a row in a table is uniquely identified by the columns in a join key\. This is used by Amazon QuickSight to optimize query performance\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)