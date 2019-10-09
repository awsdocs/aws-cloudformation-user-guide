# AWS::S3::Bucket PublicAccessBlockConfiguration<a name="aws-properties-s3-bucket-publicaccessblockconfiguration"></a>

Specifies the Block Public Access configuration for an Amazon S3 bucket\. More details in [Block Public Access Settings](https://docs.aws.amazon.com/en_us/AmazonS3/latest/dev/access-control-block-public-access.html#console-block-public-access-options)

## Syntax<a name="aws-properties-s3-bucket-publicaccessblockconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-publicaccessblockconfiguration-syntax.json"></a>

```
{
  "[BlockPublicAcls](#cfn-s3-bucket-publicaccessblockconfiguration-blockpublicacls)" : Boolean,
  "[IgnorePublicAcls](#cfn-s3-bucket-publicaccessblockconfiguration-ignorepublicacls)" : Boolean,
  "[BlockPublicPolicy](#cfn-s3-bucket-publicaccessblockconfiguration-blockpublicpolicy)" : Boolean,
  "[RestrictPublicBuckets](#cfn-s3-bucket-publicaccessblockconfiguration-restrictpublicbuckets)" : Boolean
}
```

### YAML<a name="aws-properties-s3-bucket-publicaccessblockconfiguration-syntax.yaml"></a>

```
  [BlockPublicAcls](#cfn-s3-bucket-publicaccessblockconfiguration-blockpublicacls): Boolean
  [IgnorePublicAcls](#cfn-s3-bucket-publicaccessblockconfiguration-ignorepublicacls): Boolean
  [BlockPublicPolicy](#cfn-s3-bucket-publicaccessblockconfiguration-blockpublicpolicy): Boolean
  [RestrictPublicBuckets](#cfn-s3-bucket-publicaccessblockconfiguration-restrictpublicbuckets): Boolean
```

## Properties<a name="aws-properties-s3-bucket-publicaccessblockconfiguration-properties"></a>

`BlockPublicAcls`  <a name="cfn-s3-bucket-publicaccessblockconfiguration-blockpublicacls"></a>
Specifies whether Amazon S3 should block public access control lists \(ACLs\) for this bucket and objects in this bucket\. Setting this element to `TRUE` causes the following behavior:  
+ PUT Bucket acl and PUT Object acl calls fail if the specified ACL is public\.
+ PUT Object calls fail if the request includes a public ACL\.
Enabling this setting doesn't affect existing policies or ACLs\.
This property controls the item "Block public access to buckets and objects granted through new access control lists (ACLs)" on console\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IgnorePublicAcls`  <a name="cfn-s3-bucket-publicaccessblockconfiguration-ignorepublicacls"></a>
Specifies whether Amazon S3 should ignore public ACLs for this bucket and objects in this bucket\. Setting this element to `TRUE` causes Amazon S3 to ignore all public ACLs on this bucket and objects in this bucket\.
Enabling this setting doesn't affect the persistence of any existing ACLs and doesn't prevent new public ACLs from being set\.
This property controls the item "Block public access to buckets and objects granted through any access control lists (ACLs)" on console\.
*Required*: No
*Type*: Boolean
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BlockPublicPolicy`  <a name="cfn-s3-bucket-publicaccessblockconfiguration-blockpublicpolicy"></a>
Specifies whether Amazon S3 should block public bucket policies for this bucket\. Setting this element to `TRUE` causes Amazon S3 to reject calls to PUT Bucket policy if the specified bucket policy allows public access\.   
Enabling this setting doesn't affect existing bucket policies\.  
This property controls the item "Block public access to buckets and objects granted through new public bucket policies" on console\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestrictPublicBuckets`  <a name="cfn-s3-bucket-publicaccessblockconfiguration-restrictpublicbuckets"></a>
Specifies whether Amazon S3 should restrict public bucket policies for this bucket\. Setting this element to `TRUE` restricts access to this bucket to only AWS services and authorized users within this account if the bucket has a public policy\.  
Enabling this setting doesn't affect previously stored bucket policies, except that public and cross\-account access within any public bucket policy, including non\-public delegation to specific accounts, is blocked\.  
This property controls the item "Block public and cross-account access to buckets and objects through any public bucket policies" on console\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
