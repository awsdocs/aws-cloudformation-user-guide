# AWS::QuickSight::DataSet ColumnGroup<a name="aws-properties-quicksight-dataset-columngroup"></a>

Groupings of columns that work together in certain Amazon QuickSight features\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.

## Syntax<a name="aws-properties-quicksight-dataset-columngroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-columngroup-syntax.json"></a>

```
{
  "[GeoSpatialColumnGroup](#cfn-quicksight-dataset-columngroup-geospatialcolumngroup)" : GeoSpatialColumnGroup
}
```

### YAML<a name="aws-properties-quicksight-dataset-columngroup-syntax.yaml"></a>

```
  [GeoSpatialColumnGroup](#cfn-quicksight-dataset-columngroup-geospatialcolumngroup): 
    GeoSpatialColumnGroup
```

## Properties<a name="aws-properties-quicksight-dataset-columngroup-properties"></a>

`GeoSpatialColumnGroup`  <a name="cfn-quicksight-dataset-columngroup-geospatialcolumngroup"></a>
Geospatial column group that denotes a hierarchy\.  
*Required*: No  
*Type*: [GeoSpatialColumnGroup](aws-properties-quicksight-dataset-geospatialcolumngroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)