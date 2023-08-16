# AWS::LakeFormation::Permissions DatabaseResource<a name="aws-properties-lakeformation-permissions-databaseresource"></a>

A structure for the database object\.

## Syntax<a name="aws-properties-lakeformation-permissions-databaseresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lakeformation-permissions-databaseresource-syntax.json"></a>

```
{
  "[CatalogId](#cfn-lakeformation-permissions-databaseresource-catalogid)" : String,
  "[Name](#cfn-lakeformation-permissions-databaseresource-name)" : String
}
```

### YAML<a name="aws-properties-lakeformation-permissions-databaseresource-syntax.yaml"></a>

```
  [CatalogId](#cfn-lakeformation-permissions-databaseresource-catalogid): String
  [Name](#cfn-lakeformation-permissions-databaseresource-name): String
```

## Properties<a name="aws-properties-lakeformation-permissions-databaseresource-properties"></a>

`CatalogId`  <a name="cfn-lakeformation-permissions-databaseresource-catalogid"></a>
The identifier for the Data Catalog\. By default, it is the account ID of the caller\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-lakeformation-permissions-databaseresource-name"></a>
The name of the database resource\. Unique to the Data Catalog\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)