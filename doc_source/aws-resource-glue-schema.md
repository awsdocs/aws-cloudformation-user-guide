# AWS::Glue::Schema<a name="aws-resource-glue-schema"></a>

The AWS::Glue::Schema is an AWS Glue resource type that manages schemas in the AWS Glue Schema Registry\.

## Syntax<a name="aws-resource-glue-schema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-schema-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Schema",
  "Properties" : {
      "[CheckpointVersion](#cfn-glue-schema-checkpointversion)" : SchemaVersion,
      "[Compatibility](#cfn-glue-schema-compatibility)" : String,
      "[DataFormat](#cfn-glue-schema-dataformat)" : String,
      "[Description](#cfn-glue-schema-description)" : String,
      "[Name](#cfn-glue-schema-name)" : String,
      "[Registry](#cfn-glue-schema-registry)" : Registry,
      "[SchemaDefinition](#cfn-glue-schema-schemadefinition)" : String,
      "[Tags](#cfn-glue-schema-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-glue-schema-syntax.yaml"></a>

```
Type: AWS::Glue::Schema
Properties: 
  [CheckpointVersion](#cfn-glue-schema-checkpointversion): 
    SchemaVersion
  [Compatibility](#cfn-glue-schema-compatibility): String
  [DataFormat](#cfn-glue-schema-dataformat): String
  [Description](#cfn-glue-schema-description): String
  [Name](#cfn-glue-schema-name): String
  [Registry](#cfn-glue-schema-registry): 
    Registry
  [SchemaDefinition](#cfn-glue-schema-schemadefinition): String
  [Tags](#cfn-glue-schema-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-glue-schema-properties"></a>

`CheckpointVersion`  <a name="cfn-glue-schema-checkpointversion"></a>
Specify the `VersionNumber` or the `IsLatest` for setting the checkpoint for the schema\. This is only required for updating a checkpoint\.  
*Required*: No  
*Type*: [SchemaVersion](aws-properties-glue-schema-schemaversion.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Compatibility`  <a name="cfn-glue-schema-compatibility"></a>
The compatibility mode of the schema\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataFormat`  <a name="cfn-glue-schema-dataformat"></a>
The data format of the schema definition\. Currently only `AVRO` is supported\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-glue-schema-description"></a>
A description of the schema if specified when created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-schema-name"></a>
Name of the schema to be created of max length of 255, and may only contain letters, numbers, hyphen, underscore, dollar sign, or hash mark\. No whitespace\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Registry`  <a name="cfn-glue-schema-registry"></a>
The registry where a schema is stored\.  
*Required*: No  
*Type*: [Registry](aws-properties-glue-schema-registry.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SchemaDefinition`  <a name="cfn-glue-schema-schemadefinition"></a>
The schema definition using the `DataFormat` setting for `SchemaName`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-glue-schema-tags"></a>
AWS tags that contain a key value pair and may be searched by console, command line, or API\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-glue-schema-return-values"></a>

### Ref<a name="aws-resource-glue-schema-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-glue-schema-return-values-fn--getatt"></a>

#### <a name="aws-resource-glue-schema-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the schema\.

`InitialSchemaVersionId`  <a name="InitialSchemaVersionId-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.