# AWS::Cassandra::Table ClusteringKeyColumn<a name="aws-properties-cassandra-table-clusteringkeycolumn"></a>

Defines an individual column within the clustering key\. 

## Syntax<a name="aws-properties-cassandra-table-clusteringkeycolumn-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cassandra-table-clusteringkeycolumn-syntax.json"></a>

```
{
  "[Column](#cfn-cassandra-table-clusteringkeycolumn-column)" : Column,
  "[OrderBy](#cfn-cassandra-table-clusteringkeycolumn-orderby)" : String
}
```

### YAML<a name="aws-properties-cassandra-table-clusteringkeycolumn-syntax.yaml"></a>

```
  [Column](#cfn-cassandra-table-clusteringkeycolumn-column): 
    Column
  [OrderBy](#cfn-cassandra-table-clusteringkeycolumn-orderby): String
```

## Properties<a name="aws-properties-cassandra-table-clusteringkeycolumn-properties"></a>

`Column`  <a name="cfn-cassandra-table-clusteringkeycolumn-column"></a>
The name and data type of this clustering key column\.  
*Required*: Yes  
*Type*: [Column](aws-properties-cassandra-table-column.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OrderBy`  <a name="cfn-cassandra-table-clusteringkeycolumn-orderby"></a>
The order in which this column's data will be stored:  
+ `ASC` \(default\) \- the column's data will be stored in ascending order\.
+ `DESC` \- the column's data will be stored in descending order\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)