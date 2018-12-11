# Amazon Simple Storage Service Bucket PublicAccessBlockConfiguration<a name="aws-properties-s3-bucket-publicaccessblockconfiguration"></a>

<a name="aws-properties-s3-bucket-publicaccessblockconfiguration-description"></a>The `PublicAccessBlockConfiguration` property type specifies the public access configuration for an Amazon S3 bucket\.

<a name="aws-properties-s3-bucket-publicaccessblockconfiguration-inheritance"></a> `PublicAccessBlockConfiguration` is a property of the [AWS::S3::Bucket](aws-properties-s3-bucket.md) resource type\.

## Syntax<a name="aws-properties-s3-bucket-publicaccessblockconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-publicaccessblockconfiguration-syntax.json"></a>

```
{
  "[BlockPublicAcls](#cfn-s3-bucket-publicaccessblockconfiguration-blockpublicacls)" : Boolean,
  "[BlockPublicPolicy](#cfn-s3-bucket-publicaccessblockconfiguration-blockpublicpolicy)" : Boolean,
  "[IgnorePublicAcls](#cfn-s3-bucket-publicaccessblockconfiguration-ignorepublicacls)" : Boolean,
  "[RestrictPublicBuckets](#cfn-s3-bucket-publicaccessblockconfiguration-restrictpublicbuckets)" : Boolean
}
```

### YAML<a name="aws-properties-s3-bucket-publicaccessblockconfiguration-syntax.yaml"></a>

```
[BlockPublicAcls](#cfn-s3-bucket-publicaccessblockconfiguration-blockpublicacls): Boolean
[BlockPublicPolicy](#cfn-s3-bucket-publicaccessblockconfiguration-blockpublicpolicy): Boolean
[IgnorePublicAcls](#cfn-s3-bucket-publicaccessblockconfiguration-ignorepublicacls): Boolean
[RestrictPublicBuckets](#cfn-s3-bucket-publicaccessblockconfiguration-restrictpublicbuckets): Boolean
```

## Properties<a name="aws-properties-s3-bucket-publicaccessblockconfiguration-properties"></a>

`BlockPublicAcls`  <a name="cfn-s3-bucket-publicaccessblockconfiguration-blockpublicacls"></a>
Specifies whether Amazon S3 will reject public ACLs for this bucket\.  
Enabling this setting has no effect on existing policies or ACLs\.  
 *Required*: No  
 *Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`BlockPublicPolicy`  <a name="cfn-s3-bucket-publicaccessblockconfiguration-blockpublicpolicy"></a>
Specifies whether Amazon S3 will block public bucket policies for this bucket\.  
Enabling this setting has no effect on existing policies\.  
 *Required*: No  
 *Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`IgnorePublicAcls`  <a name="cfn-s3-bucket-publicaccessblockconfiguration-ignorepublicacls"></a>
Specifies whether Amazon S3 will ignore public ACLs for this bucket\.  
 *Required*: No  
 *Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RestrictPublicBuckets`  <a name="cfn-s3-bucket-publicaccessblockconfiguration-restrictpublicbuckets"></a>
Specifies whether Amazon S3 will lock down public bucket policies for this bucket\.  
 *Required*: No  
 *Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)