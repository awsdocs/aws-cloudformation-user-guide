# AWS::EFS::FileSystem ElasticFileSystemTag<a name="aws-properties-efs-filesystem-filesystemtags"></a>

A tag is a key\-value pair attached to a file system\. Allowed characters in the `Key` and `Value` properties are letters, white space, and numbers that can be represented in UTF\-8, and the following characters:` + - = . _ : /`

## Syntax<a name="aws-properties-efs-filesystem-filesystemtags-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-efs-filesystem-filesystemtags-syntax.json"></a>

```
{
  "[Key](#cfn-efs-filesystem-filesystemtags-key)" : String,
  "[Value](#cfn-efs-filesystem-filesystemtags-value)" : String
}
```

### YAML<a name="aws-properties-efs-filesystem-filesystemtags-syntax.yaml"></a>

```
  [Key](#cfn-efs-filesystem-filesystemtags-key): String
  [Value](#cfn-efs-filesystem-filesystemtags-value): String
```

## Properties<a name="aws-properties-efs-filesystem-filesystemtags-properties"></a>

`Key`  <a name="cfn-efs-filesystem-filesystemtags-key"></a>
The tag key \(String\)\. The key can't start with `aws:`\.
*Required*: Yes
*Type*: String
*Minimum*: `1`
*Maximum*: `128`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-efs-filesystem-filesystemtags-value"></a>
The value of the tag key\.
*Required*: Yes
*Type*: String
*Maximum*: `256`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
