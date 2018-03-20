# AWS Glue Database DatabaseInput<a name="aws-properties-glue-database-databaseinput"></a>

<a name="aws-properties-glue-database-databaseinput-description"></a>The `DatabaseInput` property type specifies the metadata that is used to create or update an AWS Glue database\.

<a name="aws-properties-glue-database-databaseinput-inheritance"></a> `DatabaseInput` is a property of the [AWS::Glue::Database](aws-resource-glue-database.md) resource\.

## Syntax<a name="aws-properties-glue-database-databaseinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-database-databaseinput-syntax.json"></a>

```
{
  "[LocationUri](#cfn-glue-database-databaseinput-locationuri)" : String,
  "[Description](#cfn-glue-database-databaseinput-description)" : String,
  "[Parameters](#cfn-glue-database-databaseinput-parameters)" : JSON object,
  "[Name](#cfn-glue-database-databaseinput-name)" : String
}
```

### YAML<a name="aws-properties-glue-database-databaseinput-syntax.yaml"></a>

```
[LocationUri](#cfn-glue-database-databaseinput-locationuri): String
[Description](#cfn-glue-database-databaseinput-description): String
[Parameters](#cfn-glue-database-databaseinput-parameters): JSON object
[Name](#cfn-glue-database-databaseinput-name): String
```

## Properties<a name="aws-properties-glue-database-databaseinput-properties"></a>

For more information, see [DatabaseInput Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-databases.html#aws-glue-api-catalog-databases-DatabaseInput) in the *AWS Glue Developer Guide*\.

`LocationUri`  <a name="cfn-glue-database-databaseinput-locationuri"></a>
The location of the database \(for example, an HDFS path\)\. It must match the URI address multi\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-glue-database-databaseinput-description"></a>
The description of the database\. It must match the URI address multi\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Parameters`  <a name="cfn-glue-database-databaseinput-parameters"></a>
UTF\-8 string–to–UTF\-8 string key\-value pairs that specify the properties that are associated with the database\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-glue-database-databaseinput-name"></a>
The name of the database\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 