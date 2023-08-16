# AWS::LakeFormation::PrincipalPermissions DataCellsFilterResource<a name="aws-properties-lakeformation-principalpermissions-datacellsfilterresource"></a>

A structure that describes certain columns on certain rows\.

## Syntax<a name="aws-properties-lakeformation-principalpermissions-datacellsfilterresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-principalpermissions-datacellsfilterresource-syntax.json"></a>

```
{
  "[DatabaseName](#cfn-lakeformation-principalpermissions-datacellsfilterresource-databasename)" : String,
  "[Name](#cfn-lakeformation-principalpermissions-datacellsfilterresource-name)" : String,
  "[TableCatalogId](#cfn-lakeformation-principalpermissions-datacellsfilterresource-tablecatalogid)" : String,
  "[TableName](#cfn-lakeformation-principalpermissions-datacellsfilterresource-tablename)" : String
}
```

### YAML<a name="aws-properties-lakeformation-principalpermissions-datacellsfilterresource-syntax.yaml"></a>

```
  [DatabaseName](#cfn-lakeformation-principalpermissions-datacellsfilterresource-databasename): String
  [Name](#cfn-lakeformation-principalpermissions-datacellsfilterresource-name): String
  [TableCatalogId](#cfn-lakeformation-principalpermissions-datacellsfilterresource-tablecatalogid): String
  [TableName](#cfn-lakeformation-principalpermissions-datacellsfilterresource-tablename): String
```

## Properties<a name="aws-properties-lakeformation-principalpermissions-datacellsfilterresource-properties"></a>

`DatabaseName`  <a name="cfn-lakeformation-principalpermissions-datacellsfilterresource-databasename"></a>
A database in the Data Catalog\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-lakeformation-principalpermissions-datacellsfilterresource-name"></a>
The name given by the user to the data filter cell\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TableCatalogId`  <a name="cfn-lakeformation-principalpermissions-datacellsfilterresource-tablecatalogid"></a>
The ID of the catalog to which the table belongs\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TableName`  <a name="cfn-lakeformation-principalpermissions-datacellsfilterresource-tablename"></a>
The name of the table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)