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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-3`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
