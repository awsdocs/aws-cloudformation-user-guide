# AWS::QuickSight::DataSet FieldFolder<a name="aws-properties-quicksight-dataset-fieldfolder"></a>

A FieldFolder element is a folder that contains fields and nested subfolders\.

## Syntax<a name="aws-properties-quicksight-dataset-fieldfolder-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-fieldfolder-syntax.json"></a>

```
{
  "[Columns](#cfn-quicksight-dataset-fieldfolder-columns)" : [ String, ... ],
  "[Description](#cfn-quicksight-dataset-fieldfolder-description)" : String
}
```

### YAML<a name="aws-properties-quicksight-dataset-fieldfolder-syntax.yaml"></a>

```
  [Columns](#cfn-quicksight-dataset-fieldfolder-columns): 
    - String
  [Description](#cfn-quicksight-dataset-fieldfolder-description): String
```

## Properties<a name="aws-properties-quicksight-dataset-fieldfolder-properties"></a>

`Columns`  <a name="cfn-quicksight-dataset-fieldfolder-columns"></a>
A folder has a list of columns\. A column can only be in one folder\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-quicksight-dataset-fieldfolder-description"></a>
The description for a field folder\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)