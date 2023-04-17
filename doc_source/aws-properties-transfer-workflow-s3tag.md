# AWS::Transfer::Workflow S3Tag<a name="aws-properties-transfer-workflow-s3tag"></a>

Specifies the key\-value pair that are assigned to a file during the execution of a Tagging step\.

## Syntax<a name="aws-properties-transfer-workflow-s3tag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-workflow-s3tag-syntax.json"></a>

```
{
  "[Key](#cfn-transfer-workflow-s3tag-key)" : String,
  "[Value](#cfn-transfer-workflow-s3tag-value)" : String
}
```

### YAML<a name="aws-properties-transfer-workflow-s3tag-syntax.yaml"></a>

```
  [Key](#cfn-transfer-workflow-s3tag-key): String
  [Value](#cfn-transfer-workflow-s3tag-value): String
```

## Properties<a name="aws-properties-transfer-workflow-s3tag-properties"></a>

`Key`  <a name="cfn-transfer-workflow-s3tag-key"></a>
The name assigned to the tag that you create\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-transfer-workflow-s3tag-value"></a>
The value that corresponds to the key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)