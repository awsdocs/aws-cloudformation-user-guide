# AWS::AmazonMQ::Configuration TagsEntry<a name="aws-properties-amazonmq-configuration-tagsentry"></a>

A key\-value pair to associate with the configuration\.

## Syntax<a name="aws-properties-amazonmq-configuration-tagsentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amazonmq-configuration-tagsentry-syntax.json"></a>

```
{
  "[Key](#cfn-amazonmq-configuration-tagsentry-key)" : String,
  "[Value](#cfn-amazonmq-configuration-tagsentry-value)" : String
}
```

### YAML<a name="aws-properties-amazonmq-configuration-tagsentry-syntax.yaml"></a>

```
  [Key](#cfn-amazonmq-configuration-tagsentry-key): String
  [Value](#cfn-amazonmq-configuration-tagsentry-value): String
```

## Properties<a name="aws-properties-amazonmq-configuration-tagsentry-properties"></a>

`Key`  <a name="cfn-amazonmq-configuration-tagsentry-key"></a>
The key in a key\-value pair\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-amazonmq-configuration-tagsentry-value"></a>
The value in a key\-value pair\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)