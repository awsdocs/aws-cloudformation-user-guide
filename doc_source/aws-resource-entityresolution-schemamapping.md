# AWS::EntityResolution::SchemaMapping<a name="aws-resource-entityresolution-schemamapping"></a>

Creates a schema mapping, which defines the schema of the input customer records table\. The `SchemaMapping` also provides Entity Resolution with some metadata about the table, such as the attribute types of the columns and which columns to match on\.

## Syntax<a name="aws-resource-entityresolution-schemamapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-entityresolution-schemamapping-syntax.json"></a>

```
{
  "Type" : "AWS::EntityResolution::SchemaMapping",
  "Properties" : {
      "[Description](#cfn-entityresolution-schemamapping-description)" : String,
      "[MappedInputFields](#cfn-entityresolution-schemamapping-mappedinputfields)" : [ SchemaInputAttribute, ... ],
      "[SchemaName](#cfn-entityresolution-schemamapping-schemaname)" : String,
      "[Tags](#cfn-entityresolution-schemamapping-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-entityresolution-schemamapping-syntax.yaml"></a>

```
Type: AWS::EntityResolution::SchemaMapping
Properties: 
  [Description](#cfn-entityresolution-schemamapping-description): String
  [MappedInputFields](#cfn-entityresolution-schemamapping-mappedinputfields): 
    - SchemaInputAttribute
  [SchemaName](#cfn-entityresolution-schemamapping-schemaname): String
  [Tags](#cfn-entityresolution-schemamapping-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-entityresolution-schemamapping-properties"></a>

`Description`  <a name="cfn-entityresolution-schemamapping-description"></a>
A description of the schema\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MappedInputFields`  <a name="cfn-entityresolution-schemamapping-mappedinputfields"></a>
A list of `MappedInputFields`\. Each `MappedInputField` corresponds to a column the source data table, and contains column name plus additional information that Entity Resolution uses for matching\.  
*Required*: Yes  
*Type*: List of [SchemaInputAttribute](aws-properties-entityresolution-schemamapping-schemainputattribute.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SchemaName`  <a name="cfn-entityresolution-schemamapping-schemaname"></a>
The name of the schema\. There cannot be multiple `SchemaMappings` with the same name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-entityresolution-schemamapping-tags"></a>
The tags used to organize, track, or control access for this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)