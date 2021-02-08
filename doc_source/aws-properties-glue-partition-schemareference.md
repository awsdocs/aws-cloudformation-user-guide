# AWS::Glue::Partition SchemaReference<a name="aws-properties-glue-partition-schemareference"></a>

An object that references a schema stored in the AWS Glue Schema Registry\.

## Syntax<a name="aws-properties-glue-partition-schemareference-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-partition-schemareference-syntax.json"></a>

```
{
  "[SchameVersionId](#cfn-glue-partition-schemareference-schameversionid)" : String,
  "[SchemaId](#cfn-glue-partition-schemareference-schemaid)" : SchemaId,
  "[SchemaVersionNumber](#cfn-glue-partition-schemareference-schemaversionnumber)" : Integer
}
```

### YAML<a name="aws-properties-glue-partition-schemareference-syntax.yaml"></a>

```
  [SchameVersionId](#cfn-glue-partition-schemareference-schameversionid): String
  [SchemaId](#cfn-glue-partition-schemareference-schemaid): 
    SchemaId
  [SchemaVersionNumber](#cfn-glue-partition-schemareference-schemaversionnumber): Integer
```

## Properties<a name="aws-properties-glue-partition-schemareference-properties"></a>

`SchameVersionId`  <a name="cfn-glue-partition-schemareference-schameversionid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchemaId`  <a name="cfn-glue-partition-schemareference-schemaid"></a>
A structure that contains schema identity fields\. Either this or the `SchemaVersionId` has to be provided\.  
*Required*: No  
*Type*: [SchemaId](aws-properties-glue-partition-schemaid.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchemaVersionNumber`  <a name="cfn-glue-partition-schemareference-schemaversionnumber"></a>
The version number of the schema\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)