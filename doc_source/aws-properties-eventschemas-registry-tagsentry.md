# AWS::EventSchemas::Registry TagsEntry<a name="aws-properties-eventschemas-registry-tagsentry"></a>

Tags to associate with the schema registry\.

## Syntax<a name="aws-properties-eventschemas-registry-tagsentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eventschemas-registry-tagsentry-syntax.json"></a>

```
{
  "[Key](#cfn-eventschemas-registry-tagsentry-key)" : String,
  "[Value](#cfn-eventschemas-registry-tagsentry-value)" : String
}
```

### YAML<a name="aws-properties-eventschemas-registry-tagsentry-syntax.yaml"></a>

```
  [Key](#cfn-eventschemas-registry-tagsentry-key): String
  [Value](#cfn-eventschemas-registry-tagsentry-value): String
```

## Properties<a name="aws-properties-eventschemas-registry-tagsentry-properties"></a>

`Key`  <a name="cfn-eventschemas-registry-tagsentry-key"></a>
They key of a key\-value pair\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-eventschemas-registry-tagsentry-value"></a>
They value of a key\-value pair\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)