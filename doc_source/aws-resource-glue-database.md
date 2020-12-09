# AWS::Glue::Database<a name="aws-resource-glue-database"></a>

The `AWS::Glue::Database` resource specifies a logical grouping of tables in AWS Glue\. For more information, see [Defining a Database in Your Data Catalog](https://docs.aws.amazon.com/glue/latest/dg/define-database.html) and [Database Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-databases.html#aws-glue-api-catalog-databases-Database) in the *AWS Glue Developer Guide*\.

## Syntax<a name="aws-resource-glue-database-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-database-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Database",
  "Properties" : {
      "[CatalogId](#cfn-glue-database-catalogid)" : String,
      "[DatabaseInput](#cfn-glue-database-databaseinput)" : DatabaseInput
    }
}
```

### YAML<a name="aws-resource-glue-database-syntax.yaml"></a>

```
Type: AWS::Glue::Database
Properties: 
  [CatalogId](#cfn-glue-database-catalogid): String
  [DatabaseInput](#cfn-glue-database-databaseinput): 
    DatabaseInput
```

## Properties<a name="aws-resource-glue-database-properties"></a>

`CatalogId`  <a name="cfn-glue-database-catalogid"></a>
The AWS account ID for the account in which to create the catalog object\.  
 To specify the account ID, you can use the `Ref` intrinsic function with the `AWS::AccountId` pseudo parameter\. For example: `!Ref AWS::AccountId` 
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DatabaseInput`  <a name="cfn-glue-database-databaseinput"></a>
The metadata for the database\.  
*Required*: Yes  
*Type*: [DatabaseInput](aws-properties-glue-database-databaseinput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-glue-database-return-values"></a>

### Ref<a name="aws-resource-glue-database-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the database name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.