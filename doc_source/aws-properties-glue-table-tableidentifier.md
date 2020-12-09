# AWS::Glue::Table TableIdentifier<a name="aws-properties-glue-table-tableidentifier"></a>

A structure that describes a target table for resource linking\.

## Syntax<a name="aws-properties-glue-table-tableidentifier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-tableidentifier-syntax.json"></a>

```
{
  "[CatalogId](#cfn-glue-table-tableidentifier-catalogid)" : String,
  "[DatabaseName](#cfn-glue-table-tableidentifier-databasename)" : String,
  "[Name](#cfn-glue-table-tableidentifier-name)" : String
}
```

### YAML<a name="aws-properties-glue-table-tableidentifier-syntax.yaml"></a>

```
  [CatalogId](#cfn-glue-table-tableidentifier-catalogid): String
  [DatabaseName](#cfn-glue-table-tableidentifier-databasename): String
  [Name](#cfn-glue-table-tableidentifier-name): String
```

## Properties<a name="aws-properties-glue-table-tableidentifier-properties"></a>

`CatalogId`  <a name="cfn-glue-table-tableidentifier-catalogid"></a>
The ID of the Data Catalog in which the table resides\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-glue-table-tableidentifier-databasename"></a>
The name of the catalog database that contains the target table\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-table-tableidentifier-name"></a>
The name of the target table\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)