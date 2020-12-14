# AWS::Glue::SchemaVersionMetadata<a name="aws-resource-glue-schemaversionmetadata"></a>

The AWS::Glue::SchemaVersionMetadata is an AWS Glue resource type that defines the metadata key\-value pairs for a schema version in AWS Glue Schema Registry\.

## Syntax<a name="aws-resource-glue-schemaversionmetadata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-schemaversionmetadata-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::SchemaVersionMetadata",
  "Properties" : {
      "[Key](#cfn-glue-schemaversionmetadata-key)" : String,
      "[SchemaVersionId](#cfn-glue-schemaversionmetadata-schemaversionid)" : String,
      "[Value](#cfn-glue-schemaversionmetadata-value)" : String
    }
}
```

### YAML<a name="aws-resource-glue-schemaversionmetadata-syntax.yaml"></a>

```
Type: AWS::Glue::SchemaVersionMetadata
Properties: 
  [Key](#cfn-glue-schemaversionmetadata-key): String
  [SchemaVersionId](#cfn-glue-schemaversionmetadata-schemaversionid): String
  [Value](#cfn-glue-schemaversionmetadata-value): String
```

## Properties<a name="aws-resource-glue-schemaversionmetadata-properties"></a>

`Key`  <a name="cfn-glue-schemaversionmetadata-key"></a>
A metadata key in a key\-value pair for metadata\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SchemaVersionId`  <a name="cfn-glue-schemaversionmetadata-schemaversionid"></a>
The version number of the schema\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-glue-schemaversionmetadata-value"></a>
A metadata key's corresponding value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-glue-schemaversionmetadata-return-values"></a>

### Ref<a name="aws-resource-glue-schemaversionmetadata-return-values-ref"></a>