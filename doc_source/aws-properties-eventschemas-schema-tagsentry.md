# AWS::EventSchemas::Schema TagsEntry<a name="aws-properties-eventschemas-schema-tagsentry"></a>

Tags to associate with the schema\.

## Syntax<a name="aws-properties-eventschemas-schema-tagsentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eventschemas-schema-tagsentry-syntax.json"></a>

```
{
  "[Key](#cfn-eventschemas-schema-tagsentry-key)" : String,
  "[Value](#cfn-eventschemas-schema-tagsentry-value)" : String
}
```

### YAML<a name="aws-properties-eventschemas-schema-tagsentry-syntax.yaml"></a>

```
  [Key](#cfn-eventschemas-schema-tagsentry-key): String
  [Value](#cfn-eventschemas-schema-tagsentry-value): String
```

## Properties<a name="aws-properties-eventschemas-schema-tagsentry-properties"></a>

`Key`  <a name="cfn-eventschemas-schema-tagsentry-key"></a>
They key of a key\-value pair\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-eventschemas-schema-tagsentry-value"></a>
They value of a key\-value pair\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)