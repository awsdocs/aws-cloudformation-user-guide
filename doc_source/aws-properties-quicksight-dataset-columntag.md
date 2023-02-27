# AWS::QuickSight::DataSet ColumnTag<a name="aws-properties-quicksight-dataset-columntag"></a>

A tag for a column in a ` [TagColumnOperation](https://docs.aws.amazon.com/quicksight/latest/APIReference/API_TagColumnOperation.html) ` structure\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.

## Syntax<a name="aws-properties-quicksight-dataset-columntag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-columntag-syntax.json"></a>

```
{
  "[ColumnDescription](#cfn-quicksight-dataset-columntag-columndescription)" : ColumnDescription,
  "[ColumnGeographicRole](#cfn-quicksight-dataset-columntag-columngeographicrole)" : String
}
```

### YAML<a name="aws-properties-quicksight-dataset-columntag-syntax.yaml"></a>

```
  [ColumnDescription](#cfn-quicksight-dataset-columntag-columndescription): 
    ColumnDescription
  [ColumnGeographicRole](#cfn-quicksight-dataset-columntag-columngeographicrole): String
```

## Properties<a name="aws-properties-quicksight-dataset-columntag-properties"></a>

`ColumnDescription`  <a name="cfn-quicksight-dataset-columntag-columndescription"></a>
A description for a column\.  
*Required*: No  
*Type*: [ColumnDescription](aws-properties-quicksight-dataset-columndescription.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnGeographicRole`  <a name="cfn-quicksight-dataset-columntag-columngeographicrole"></a>
A geospatial role for a column\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CITY | COUNTRY | COUNTY | LATITUDE | LONGITUDE | POSTCODE | STATE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)