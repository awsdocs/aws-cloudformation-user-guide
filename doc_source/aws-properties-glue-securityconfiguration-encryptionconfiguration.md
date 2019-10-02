# AWS::Glue::SecurityConfiguration EncryptionConfiguration<a name="aws-properties-glue-securityconfiguration-encryptionconfiguration"></a>

Specifies an encryption configuration\.

## Syntax<a name="aws-properties-glue-securityconfiguration-encryptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-securityconfiguration-encryptionconfiguration-syntax.json"></a>

```
{
  "[CloudWatchEncryption](#cfn-glue-securityconfiguration-encryptionconfiguration-cloudwatchencryption)" : [CloudWatchEncryption](aws-properties-glue-securityconfiguration-cloudwatchencryption.md),
  "[JobBookmarksEncryption](#cfn-glue-securityconfiguration-encryptionconfiguration-jobbookmarksencryption)" : [JobBookmarksEncryption](aws-properties-glue-securityconfiguration-jobbookmarksencryption.md),
  "[S3Encryptions](#cfn-glue-securityconfiguration-encryptionconfiguration-s3encryptions)" : [ [S3Encryption](aws-properties-glue-securityconfiguration-s3encryption.md), ... ]
}
```

### YAML<a name="aws-properties-glue-securityconfiguration-encryptionconfiguration-syntax.yaml"></a>

```
  [CloudWatchEncryption](#cfn-glue-securityconfiguration-encryptionconfiguration-cloudwatchencryption): 
    [CloudWatchEncryption](aws-properties-glue-securityconfiguration-cloudwatchencryption.md)
  [JobBookmarksEncryption](#cfn-glue-securityconfiguration-encryptionconfiguration-jobbookmarksencryption): 
    [JobBookmarksEncryption](aws-properties-glue-securityconfiguration-jobbookmarksencryption.md)
  [S3Encryptions](#cfn-glue-securityconfiguration-encryptionconfiguration-s3encryptions): 
    - [S3Encryption](aws-properties-glue-securityconfiguration-s3encryption.md)
```

## Properties<a name="aws-properties-glue-securityconfiguration-encryptionconfiguration-properties"></a>

`CloudWatchEncryption`  <a name="cfn-glue-securityconfiguration-encryptionconfiguration-cloudwatchencryption"></a>
The encryption configuration for Amazon CloudWatch\.  
*Required*: No  
*Type*: [CloudWatchEncryption](aws-properties-glue-securityconfiguration-cloudwatchencryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobBookmarksEncryption`  <a name="cfn-glue-securityconfiguration-encryptionconfiguration-jobbookmarksencryption"></a>
The encryption configuration for job bookmarks\.  
*Required*: No  
*Type*: [JobBookmarksEncryption](aws-properties-glue-securityconfiguration-jobbookmarksencryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Encryptions`  <a name="cfn-glue-securityconfiguration-encryptionconfiguration-s3encryptions"></a>
The encyption configuration for Amazon Simple Storage Service \(Amazon S3\) data\.  
*Required*: No  
*Type*: [List](aws-properties-glue-securityconfiguration-s3encryptions.md) of [S3Encryption](aws-properties-glue-securityconfiguration-s3encryption.md)  
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
- `eu-west-2`
- `eu-west-3`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
