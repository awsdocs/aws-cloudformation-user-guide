# AWS::LakeFormation::TagAssociation TableResource<a name="aws-properties-lakeformation-tagassociation-tableresource"></a>

A structure for the table object\. A table is a metadata definition that represents your data\. You can Grant and Revoke table privileges to a principal\. 

## Syntax<a name="aws-properties-lakeformation-tagassociation-tableresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-tagassociation-tableresource-syntax.json"></a>

```
{
  "[CatalogId](#cfn-lakeformation-tagassociation-tableresource-catalogid)" : String,
  "[DatabaseName](#cfn-lakeformation-tagassociation-tableresource-databasename)" : String,
  "[Name](#cfn-lakeformation-tagassociation-tableresource-name)" : String,
  "[TableWildcard](#cfn-lakeformation-tagassociation-tableresource-tablewildcard)" : Json
}
```

### YAML<a name="aws-properties-lakeformation-tagassociation-tableresource-syntax.yaml"></a>

```
  [CatalogId](#cfn-lakeformation-tagassociation-tableresource-catalogid): String
  [DatabaseName](#cfn-lakeformation-tagassociation-tableresource-databasename): String
  [Name](#cfn-lakeformation-tagassociation-tableresource-name): String
  [TableWildcard](#cfn-lakeformation-tagassociation-tableresource-tablewildcard): Json
```

## Properties<a name="aws-properties-lakeformation-tagassociation-tableresource-properties"></a>

`CatalogId`  <a name="cfn-lakeformation-tagassociation-tableresource-catalogid"></a>
The identifier for the Data Catalog\. By default, it is the account ID of the caller\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DatabaseName`  <a name="cfn-lakeformation-tagassociation-tableresource-databasename"></a>
The name of the database for the table\. Unique to a Data Catalog\. A database is a set of associated table definitions organized into a logical group\. You can Grant and Revoke database privileges to a principal\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-lakeformation-tagassociation-tableresource-name"></a>
The name of the table\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TableWildcard`  <a name="cfn-lakeformation-tagassociation-tableresource-tablewildcard"></a>
A wildcard object representing every table under a database\.This is an object with no properties that effectively behaves as a true or false depending on whether not it is passed as a parameter\. The valid inputs for a property with this type in either yaml or json is null or \{\}\.  
At least one of `TableResource$Name` or `TableResource$TableWildcard` is required\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)