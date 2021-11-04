# AWS::Glue::Table SchemaReference<a name="aws-properties-glue-table-schemareference"></a>

An object that references a schema stored in the AWS Glue Schema Registry\.

## Syntax<a name="aws-properties-glue-table-schemareference-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-schemareference-syntax.json"></a>

```
{
  "[SchemaId](#cfn-glue-table-schemareference-schemaid)" : SchemaId,
  "[SchemaVersionId](#cfn-glue-table-schemareference-schemaversionid)" : String,
  "[SchemaVersionNumber](#cfn-glue-table-schemareference-schemaversionnumber)" : Integer
}
```

### YAML<a name="aws-properties-glue-table-schemareference-syntax.yaml"></a>

```
  [SchemaId](#cfn-glue-table-schemareference-schemaid): 
    SchemaId
  [SchemaVersionId](#cfn-glue-table-schemareference-schemaversionid): String
  [SchemaVersionNumber](#cfn-glue-table-schemareference-schemaversionnumber): Integer
```

## Properties<a name="aws-properties-glue-table-schemareference-properties"></a>

`SchemaId`  <a name="cfn-glue-table-schemareference-schemaid"></a>
A structure that contains schema identity fields\. Either this or the `SchemaVersionId` has to be provided\.  
*Required*: No  
*Type*: [SchemaId](aws-properties-glue-table-schemaid.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchemaVersionId`  <a name="cfn-glue-table-schemareference-schemaversionid"></a>
The unique ID assigned to a version of the schema\. Either this or the `SchemaId` has to be provided\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchemaVersionNumber`  <a name="cfn-glue-table-schemareference-schemaversionnumber"></a>
The version number of the schema\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)