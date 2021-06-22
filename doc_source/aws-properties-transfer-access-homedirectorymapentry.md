# AWS::Transfer::Access HomeDirectoryMapEntry<a name="aws-properties-transfer-access-homedirectorymapentry"></a>

Represents an object that contains entries and targets for `HomeDirectoryMappings`\.

The following is an `Entry` and `Target` pair example for `chroot`\.

 `[ { "Entry:": "/", "Target": "/bucket_name/home/mydirectory" } ]` 

**Note**  
If the target of a logical directory entry does not exist in Amazon S3 or EFS, the entry is ignored\. As a workaround, you can use the Amazon S3 API or EFS API to create 0 byte objects as place holders for your directory\. If using the CLI, use the `s3api` or `efsapi` call instead of `s3` or `efs` so you can use the put\-object operation\. For example, you use the following: `aws s3api put-object --bucket bucketname --key path/to/folder/`\. Make sure that the end of the key name ends in a `/` for it to be considered a folder\.

## Syntax<a name="aws-properties-transfer-access-homedirectorymapentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-access-homedirectorymapentry-syntax.json"></a>

```
{
  "[Entry](#cfn-transfer-access-homedirectorymapentry-entry)" : String,
  "[Target](#cfn-transfer-access-homedirectorymapentry-target)" : String
}
```

### YAML<a name="aws-properties-transfer-access-homedirectorymapentry-syntax.yaml"></a>

```
  [Entry](#cfn-transfer-access-homedirectorymapentry-entry): String
  [Target](#cfn-transfer-access-homedirectorymapentry-target): String
```

## Properties<a name="aws-properties-transfer-access-homedirectorymapentry-properties"></a>

`Entry`  <a name="cfn-transfer-access-homedirectorymapentry-entry"></a>
Represents an entry for `HomeDirectoryMappings`\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-transfer-access-homedirectorymapentry-target"></a>
Represents the map target that is used in a `HomeDirectorymapEntry`\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)