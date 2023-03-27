# AWS::LakeFormation::TagAssociation Resource<a name="aws-properties-lakeformation-tagassociation-resource"></a>

A structure for the resource\.

## Syntax<a name="aws-properties-lakeformation-tagassociation-resource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-tagassociation-resource-syntax.json"></a>

```
{
  "[Catalog](#cfn-lakeformation-tagassociation-resource-catalog)" : Json,
  "[Database](#cfn-lakeformation-tagassociation-resource-database)" : DatabaseResource,
  "[Table](#cfn-lakeformation-tagassociation-resource-table)" : TableResource,
  "[TableWithColumns](#cfn-lakeformation-tagassociation-resource-tablewithcolumns)" : TableWithColumnsResource
}
```

### YAML<a name="aws-properties-lakeformation-tagassociation-resource-syntax.yaml"></a>

```
  [Catalog](#cfn-lakeformation-tagassociation-resource-catalog): Json
  [Database](#cfn-lakeformation-tagassociation-resource-database): 
    DatabaseResource
  [Table](#cfn-lakeformation-tagassociation-resource-table): 
    TableResource
  [TableWithColumns](#cfn-lakeformation-tagassociation-resource-tablewithcolumns): 
    TableWithColumnsResource
```

## Properties<a name="aws-properties-lakeformation-tagassociation-resource-properties"></a>

`Catalog`  <a name="cfn-lakeformation-tagassociation-resource-catalog"></a>
The identifier for the Data Catalog\. By default, the account ID\. The Data Catalog is the persistent metadata store\. It contains database definitions, table definitions, and other control information to manage your AWS Lake Formation environment\.   
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Database`  <a name="cfn-lakeformation-tagassociation-resource-database"></a>
The database for the resource\. Unique to the Data Catalog\. A database is a set of associated table definitions organized into a logical group\. You can Grant and Revoke database permissions to a principal\.   
*Required*: No  
*Type*: [DatabaseResource](aws-properties-lakeformation-tagassociation-databaseresource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Table`  <a name="cfn-lakeformation-tagassociation-resource-table"></a>
The table for the resource\. A table is a metadata definition that represents your data\. You can Grant and Revoke table privileges to a principal\.   
*Required*: No  
*Type*: [TableResource](aws-properties-lakeformation-tagassociation-tableresource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TableWithColumns`  <a name="cfn-lakeformation-tagassociation-resource-tablewithcolumns"></a>
The table with columns for the resource\. A principal with permissions to this resource can select metadata from the columns of a table in the Data Catalog and the underlying data in Amazon S3\.  
*Required*: No  
*Type*: [TableWithColumnsResource](aws-properties-lakeformation-tagassociation-tablewithcolumnsresource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)