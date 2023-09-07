# AWS::QuickSight::Template TableStyleTarget<a name="aws-properties-quicksight-template-tablestyletarget"></a>

The table style target\.

## Syntax<a name="aws-properties-quicksight-template-tablestyletarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-tablestyletarget-syntax.json"></a>

```
{
  "[CellType](#cfn-quicksight-template-tablestyletarget-celltype)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-tablestyletarget-syntax.yaml"></a>

```
  [CellType](#cfn-quicksight-template-tablestyletarget-celltype): String
```

## Properties<a name="aws-properties-quicksight-template-tablestyletarget-properties"></a>

`CellType`  <a name="cfn-quicksight-template-tablestyletarget-celltype"></a>
The cell type of the table style target\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `METRIC_HEADER | TOTAL | VALUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)