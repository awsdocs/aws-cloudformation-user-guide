# AWS::Glue::Database<a name="aws-resource-glue-database"></a>

The `AWS::Glue::Database` resource specifies a logical grouping of tables in AWS Glue\. For more information, see [Defining a Database in Your Data Catalog](http://docs.aws.amazon.com/glue/latest/dg/define-database.html) and [Database Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-databases.html#aws-glue-api-catalog-databases-Database) in the *AWS Glue Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-glue-database-syntax)
+ [Properties](#aws-resource-glue-database-properties)
+ [Return Values](#aws-resource-glue-database-returnvalues)

## Syntax<a name="aws-resource-glue-database-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-database-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Database",
  "Properties" : {
    "[DatabaseInput](#cfn-glue-database-databaseinput)" : [*DatabaseInput*](aws-properties-glue-database-databaseinput.md),
    "[CatalogId](#cfn-glue-database-catalogid)" : String
  }
}
```

### YAML<a name="aws-resource-glue-database-syntax.yaml"></a>

```
Type: "AWS::Glue::Database"
Properties:
  [DatabaseInput](#cfn-glue-database-databaseinput): 
    [*DatabaseInput*](aws-properties-glue-database-databaseinput.md)
  [CatalogId](#cfn-glue-database-catalogid): String
```

## Properties<a name="aws-resource-glue-database-properties"></a>

`DatabaseInput`  <a name="cfn-glue-database-databaseinput"></a>
The metadata of the database\.  
 *Required*: Yes  
 *Type*: [AWS Glue Database DatabaseInput](aws-properties-glue-database-databaseinput.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`CatalogId`  <a name="cfn-glue-database-catalogid"></a>
The ID of the data catalog to create the catalog object in\. Currently, this should be the AWS account ID\.  
To specify the account ID, you can use the `Ref` intrinsic function with the `AWS::AccountId` pseudo parameter—for example `!Ref AWS::AccountId`\.
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-glue-database-returnvalues"></a>

### Ref<a name="w3ab2c21c10d707c11b3"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the `DatabaseInput` name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 