# AWS::LakeFormation::Permissions TableResource<a name="aws-properties-lakeformation-permissions-tableresource"></a>

A structure for the table object\. A table is a metadata definition that represents your data\. You can Grant and Revoke table privileges to a principal\. 

## Syntax<a name="aws-properties-lakeformation-permissions-tableresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-permissions-tableresource-syntax.json"></a>

```
{
  "[CatalogId](#cfn-lakeformation-permissions-tableresource-catalogid)" : String,
  "[DatabaseName](#cfn-lakeformation-permissions-tableresource-databasename)" : String,
  "[Name](#cfn-lakeformation-permissions-tableresource-name)" : String,
  "[TableWildcard](#cfn-lakeformation-permissions-tableresource-tablewildcard)" : TableWildcard
}
```

### YAML<a name="aws-properties-lakeformation-permissions-tableresource-syntax.yaml"></a>

```
  [CatalogId](#cfn-lakeformation-permissions-tableresource-catalogid): String
  [DatabaseName](#cfn-lakeformation-permissions-tableresource-databasename): String
  [Name](#cfn-lakeformation-permissions-tableresource-name): String
  [TableWildcard](#cfn-lakeformation-permissions-tableresource-tablewildcard): 
    TableWildcard
```

## Properties<a name="aws-properties-lakeformation-permissions-tableresource-properties"></a>

`CatalogId`  <a name="cfn-lakeformation-permissions-tableresource-catalogid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-lakeformation-permissions-tableresource-databasename"></a>
The name of the database for the table\. Unique to a Data Catalog\. A database is a set of associated table definitions organized into a logical group\. You can Grant and Revoke database privileges to a principal\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-lakeformation-permissions-tableresource-name"></a>
The name of the table\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableWildcard`  <a name="cfn-lakeformation-permissions-tableresource-tablewildcard"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [TableWildcard](aws-properties-lakeformation-permissions-tablewildcard.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)