# AWS::LakeFormation::Permissions TableWithColumnsResource<a name="aws-properties-lakeformation-permissions-tablewithcolumnsresource"></a>

A structure for a table with columns object\. This object is only used when granting a SELECT permission\.

This object must take a value for at least one of `ColumnsNames`, `ColumnsIndexes`, or `ColumnsWildcard`\.

## Syntax<a name="aws-properties-lakeformation-permissions-tablewithcolumnsresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-permissions-tablewithcolumnsresource-syntax.json"></a>

```
{
  "[CatalogId](#cfn-lakeformation-permissions-tablewithcolumnsresource-catalogid)" : String,
  "[ColumnNames](#cfn-lakeformation-permissions-tablewithcolumnsresource-columnnames)" : [ String, ... ],
  "[ColumnWildcard](#cfn-lakeformation-permissions-tablewithcolumnsresource-columnwildcard)" : ColumnWildcard,
  "[DatabaseName](#cfn-lakeformation-permissions-tablewithcolumnsresource-databasename)" : String,
  "[Name](#cfn-lakeformation-permissions-tablewithcolumnsresource-name)" : String
}
```

### YAML<a name="aws-properties-lakeformation-permissions-tablewithcolumnsresource-syntax.yaml"></a>

```
  [CatalogId](#cfn-lakeformation-permissions-tablewithcolumnsresource-catalogid): String
  [ColumnNames](#cfn-lakeformation-permissions-tablewithcolumnsresource-columnnames): 
    - String
  [ColumnWildcard](#cfn-lakeformation-permissions-tablewithcolumnsresource-columnwildcard): 
    ColumnWildcard
  [DatabaseName](#cfn-lakeformation-permissions-tablewithcolumnsresource-databasename): String
  [Name](#cfn-lakeformation-permissions-tablewithcolumnsresource-name): String
```

## Properties<a name="aws-properties-lakeformation-permissions-tablewithcolumnsresource-properties"></a>

`CatalogId`  <a name="cfn-lakeformation-permissions-tablewithcolumnsresource-catalogid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnNames`  <a name="cfn-lakeformation-permissions-tablewithcolumnsresource-columnnames"></a>
The list of column names for the table\. At least one of `ColumnNames` or `ColumnWildcard` is required\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnWildcard`  <a name="cfn-lakeformation-permissions-tablewithcolumnsresource-columnwildcard"></a>
A wildcard specified by a `ColumnWildcard` object\. At least one of `ColumnNames` or `ColumnWildcard` is required\.  
*Required*: No  
*Type*: [ColumnWildcard](aws-properties-lakeformation-permissions-columnwildcard.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-lakeformation-permissions-tablewithcolumnsresource-databasename"></a>
The name of the database for the table with columns resource\. Unique to the Data Catalog\. A database is a set of associated table definitions organized into a logical group\. You can Grant and Revoke database privileges to a principal\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-lakeformation-permissions-tablewithcolumnsresource-name"></a>
The name of the table resource\. A table is a metadata definition that represents your data\. You can Grant and Revoke table privileges to a principal\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)