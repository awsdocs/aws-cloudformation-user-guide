# AWS::Glue::SchemaVersion<a name="aws-resource-glue-schemaversion"></a>

The AWS::Glue::SchemaVersion is an AWS Glue resource type that manages schema versions of schemas in the AWS Glue Schema Registry\.

## Syntax<a name="aws-resource-glue-schemaversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-schemaversion-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::SchemaVersion",
  "Properties" : {
      "[Schema](#cfn-glue-schemaversion-schema)" : Schema,
      "[SchemaDefinition](#cfn-glue-schemaversion-schemadefinition)" : String
    }
}
```

### YAML<a name="aws-resource-glue-schemaversion-syntax.yaml"></a>

```
Type: AWS::Glue::SchemaVersion
Properties: 
  [Schema](#cfn-glue-schemaversion-schema): 
    Schema
  [SchemaDefinition](#cfn-glue-schemaversion-schemadefinition): String
```

## Properties<a name="aws-resource-glue-schemaversion-properties"></a>

`Schema`  <a name="cfn-glue-schemaversion-schema"></a>
The schema that includes the schema version\.  
*Required*: Yes  
*Type*: [Schema](aws-properties-glue-schemaversion-schema.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SchemaDefinition`  <a name="cfn-glue-schemaversion-schemadefinition"></a>
The schema definition for the schema version\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-glue-schemaversion-return-values"></a>

### Ref<a name="aws-resource-glue-schemaversion-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-glue-schemaversion-return-values-fn--getatt"></a>

#### <a name="aws-resource-glue-schemaversion-return-values-fn--getatt-fn--getatt"></a>

`VersionId`  <a name="VersionId-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.