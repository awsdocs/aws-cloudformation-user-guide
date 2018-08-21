# Amazon Elastic File System FileSystem FileSystemTags<a name="aws-properties-efs-filesystem-filesystemtags"></a>

`FileSystemTags` is a property of the [AWS::EFS::FileSystem](aws-resource-efs-filesystem.md) resource that associates key\-value pairs with a file system\. You can use any of the following Unicode characters for keys and values: letters, digits, whitespace, \_, \., /, =, \+, and \-\.

## Syntax<a name="w3ab2c21c14d918b5"></a>

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

## Properties<a name="w3ab2c21c14d918b7"></a>

`Key`  <a name="cfn-efs-filesystem-filesystemtags-key"></a>
The key name of the tag\. You can specify a value that is from 1 to 128 Unicode characters in length, but you cannot use the prefix `aws:`\.  
*Required*: No  
*Type*: String

`Value`  <a name="cfn-efs-filesystem-filesystemtags-value"></a>
The value of the tag key\. You can specify a value that is from 0 to 128 Unicode characters in length\.  
*Required*: No  
*Type*: String