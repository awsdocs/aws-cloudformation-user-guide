# AWS::QuickSight::DataSet OutputColumn<a name="aws-properties-quicksight-dataset-outputcolumn"></a>

Output column\.

## Syntax<a name="aws-properties-quicksight-dataset-outputcolumn-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-outputcolumn-syntax.json"></a>

```
{
  "[Description](#cfn-quicksight-dataset-outputcolumn-description)" : String,
  "[Name](#cfn-quicksight-dataset-outputcolumn-name)" : String,
  "[Type](#cfn-quicksight-dataset-outputcolumn-type)" : String
}
```

### YAML<a name="aws-properties-quicksight-dataset-outputcolumn-syntax.yaml"></a>

```
  [Description](#cfn-quicksight-dataset-outputcolumn-description): String
  [Name](#cfn-quicksight-dataset-outputcolumn-name): String
  [Type](#cfn-quicksight-dataset-outputcolumn-type): String
```

## Properties<a name="aws-properties-quicksight-dataset-outputcolumn-properties"></a>

`Description`  <a name="cfn-quicksight-dataset-outputcolumn-description"></a>
A description for a column\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-dataset-outputcolumn-name"></a>
A display name for the dataset\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-dataset-outputcolumn-type"></a>
Type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DATETIME | DECIMAL | INTEGER | STRING`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)