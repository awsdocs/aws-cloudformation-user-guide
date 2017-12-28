# AWS::Glue::Table<a name="aws-resource-glue-table"></a>

The `AWS::Glue::Table` resource specifies tabular data in the AWS Glue data catalog\. For more information, see [Defining Tables in the AWS Glue Data Catalog](http://docs.aws.amazon.com/glue/latest/dg/tables-described.html) and [Table Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-Table) in the *AWS Glue Developer Guide*\. 


+ [Syntax](#aws-resource-glue-table-syntax)
+ [Properties](#aws-resource-glue-table-properties)
+ [Return Values](#aws-resource-glue-table-returnvalues)

## Syntax<a name="aws-resource-glue-table-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-table-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Table",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput)" : TableInput,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-databasename)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-catalogid)" : String
  }
}
```

### YAML<a name="aws-resource-glue-table-syntax.yaml"></a>

```
Type: "AWS::Glue::Table"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-tableinput): 
    TableInput
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-databasename): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-table-catalogid): String
```

## Properties<a name="aws-resource-glue-table-properties"></a>

`TableInput`  
The metadata of the table\.  
 *Required*: Yes  
 *Type*:   
 *Update requires*: Some interruptions 

`DatabaseName`  
The name of the catalog database for the table\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: Replacement 

`CatalogId`  
The ID of the data catalog to create the catalog object in\. Currently, this should be the AWS account ID\.  
To specify the account ID, you can use the `Ref` intrinsic function with the `AWS::AccountId` pseudo parameter—for example `!Ref AWS::AccountId`\.
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

## Return Values<a name="aws-resource-glue-table-returnvalues"></a>

### Ref<a name="w3ab2c21c10d675c10b3"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the `TableInput` name\.

For more information about using the `Ref` function, see Ref\. 