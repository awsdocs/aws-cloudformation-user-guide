# AWS::Glue::Table<a name="aws-resource-glue-table"></a>

The `AWS::Glue::Table` resource specifies tabular data in the AWS Glue data catalog\. For more information, see [Defining Tables in the AWS Glue Data Catalog](https://docs.aws.amazon.com/glue/latest/dg/tables-described.html) and [Table Structure ](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-tables.html#aws-glue-api-catalog-tables-Table) in the *AWS Glue Developer Guide*\.

## Syntax<a name="aws-resource-glue-table-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-table-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Table",
  "Properties" : {
      "[CatalogId](#cfn-glue-table-catalogid)" : String,
      "[DatabaseName](#cfn-glue-table-databasename)" : String,
      "[TableInput](#cfn-glue-table-tableinput)" : [TableInput](aws-properties-glue-table-tableinput.md)
    }
}
```

### YAML<a name="aws-resource-glue-table-syntax.yaml"></a>

```
Type: AWS::Glue::Table
Properties: 
  [CatalogId](#cfn-glue-table-catalogid): String
  [DatabaseName](#cfn-glue-table-databasename): String
  [TableInput](#cfn-glue-table-tableinput): 
    [TableInput](aws-properties-glue-table-tableinput.md)
```

## Properties<a name="aws-resource-glue-table-properties"></a>

`CatalogId`  <a name="cfn-glue-table-catalogid"></a>
The ID of the Data Catalog in which to create the `Table`\. If none is supplied, the AWS account ID is used by default\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DatabaseName`  <a name="cfn-glue-table-databasename"></a>
The name of the database where the table metadata resides\. For Hive compatibility, this must be all lowercase\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TableInput`  <a name="cfn-glue-table-tableinput"></a>
A structure used to define a table\.  
*Required*: Yes  
*Type*: [TableInput](aws-properties-glue-table-tableinput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-glue-table-return-values"></a>

### Ref<a name="aws-resource-glue-table-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the table name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
