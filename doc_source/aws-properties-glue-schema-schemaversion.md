# AWS::Glue::Schema SchemaVersion<a name="aws-properties-glue-schema-schemaversion"></a>

Specifies the version of a schema\.

## Syntax<a name="aws-properties-glue-schema-schemaversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-schema-schemaversion-syntax.json"></a>

```
{
  "[IsLatest](#cfn-glue-schema-schemaversion-islatest)" : Boolean,
  "[VersionNumber](#cfn-glue-schema-schemaversion-versionnumber)" : Integer
}
```

### YAML<a name="aws-properties-glue-schema-schemaversion-syntax.yaml"></a>

```
  [IsLatest](#cfn-glue-schema-schemaversion-islatest): Boolean
  [VersionNumber](#cfn-glue-schema-schemaversion-versionnumber): Integer
```

## Properties<a name="aws-properties-glue-schema-schemaversion-properties"></a>

`IsLatest`  <a name="cfn-glue-schema-schemaversion-islatest"></a>
Indicates if this version is the latest version of the schema\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VersionNumber`  <a name="cfn-glue-schema-schemaversion-versionnumber"></a>
The version number of the schema\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)