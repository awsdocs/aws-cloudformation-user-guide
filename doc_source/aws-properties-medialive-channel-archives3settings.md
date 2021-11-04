# AWS::MediaLive::Channel ArchiveS3Settings<a name="aws-properties-medialive-channel-archives3settings"></a>

Sets up Amazon S3 as the destination for this Archive output\.

The parent of this entity is ArchiveCdnSettings\.

## Syntax<a name="aws-properties-medialive-channel-archives3settings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-archives3settings-syntax.json"></a>

```
{
  "[CannedAcl](#cfn-medialive-channel-archives3settings-cannedacl)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-archives3settings-syntax.yaml"></a>

```
  [CannedAcl](#cfn-medialive-channel-archives3settings-cannedacl): String
```

## Properties<a name="aws-properties-medialive-channel-archives3settings-properties"></a>

`CannedAcl`  <a name="cfn-medialive-channel-archives3settings-cannedacl"></a>
Specify the canned ACL to apply to each S3 request\. Defaults to none\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)