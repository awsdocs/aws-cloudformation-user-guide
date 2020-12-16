# AWS::S3::Bucket SseKmsEncryptedObjects<a name="aws-properties-s3-bucket-ssekmsencryptedobjects"></a>

A container for filter information for the selection of S3 objects encrypted with AWS KMS\.

## Syntax<a name="aws-properties-s3-bucket-ssekmsencryptedobjects-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-ssekmsencryptedobjects-syntax.json"></a>

```
{
  "[Status](#cfn-s3-bucket-ssekmsencryptedobjects-status)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-ssekmsencryptedobjects-syntax.yaml"></a>

```
  [Status](#cfn-s3-bucket-ssekmsencryptedobjects-status): String
```

## Properties<a name="aws-properties-s3-bucket-ssekmsencryptedobjects-properties"></a>

`Status`  <a name="cfn-s3-bucket-ssekmsencryptedobjects-status"></a>
Specifies whether Amazon S3 replicates objects created with server\-side encryption using a customer master key \(CMK\) stored in AWS Key Management Service\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)