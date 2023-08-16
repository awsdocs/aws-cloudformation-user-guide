# AWS::S3ObjectLambda::AccessPoint PublicAccessBlockConfiguration<a name="aws-properties-s3objectlambda-accesspoint-publicaccessblockconfiguration"></a>

The `PublicAccessBlock` configuration that you want to apply to this Amazon S3 account\. You can enable the configuration options in any combination\. For more information about when Amazon S3 considers a bucket or object public, see [The Meaning of "Public"](https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html#access-control-block-public-access-policy-status) in the *Amazon S3 User Guide*\.

This data type is not supported for Amazon S3 on Outposts\.

## Syntax<a name="aws-properties-s3objectlambda-accesspoint-publicaccessblockconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3objectlambda-accesspoint-publicaccessblockconfiguration-syntax.json"></a>

```
{
  "[BlockPublicAcls](#cfn-s3objectlambda-accesspoint-publicaccessblockconfiguration-blockpublicacls)" : Boolean,
  "[BlockPublicPolicy](#cfn-s3objectlambda-accesspoint-publicaccessblockconfiguration-blockpublicpolicy)" : Boolean,
  "[IgnorePublicAcls](#cfn-s3objectlambda-accesspoint-publicaccessblockconfiguration-ignorepublicacls)" : Boolean,
  "[RestrictPublicBuckets](#cfn-s3objectlambda-accesspoint-publicaccessblockconfiguration-restrictpublicbuckets)" : Boolean
}
```

### YAML<a name="aws-properties-s3objectlambda-accesspoint-publicaccessblockconfiguration-syntax.yaml"></a>

```
  [BlockPublicAcls](#cfn-s3objectlambda-accesspoint-publicaccessblockconfiguration-blockpublicacls): Boolean
  [BlockPublicPolicy](#cfn-s3objectlambda-accesspoint-publicaccessblockconfiguration-blockpublicpolicy): Boolean
  [IgnorePublicAcls](#cfn-s3objectlambda-accesspoint-publicaccessblockconfiguration-ignorepublicacls): Boolean
  [RestrictPublicBuckets](#cfn-s3objectlambda-accesspoint-publicaccessblockconfiguration-restrictpublicbuckets): Boolean
```

## Properties<a name="aws-properties-s3objectlambda-accesspoint-publicaccessblockconfiguration-properties"></a>

`BlockPublicAcls`  <a name="cfn-s3objectlambda-accesspoint-publicaccessblockconfiguration-blockpublicacls"></a>
Specifies whether Amazon S3 should block public access control lists \(ACLs\) for buckets in this account\. Setting this element to `TRUE` causes the following behavior:  
+  `PutBucketAcl` and `PutObjectAcl` calls fail if the specified ACL is public\.
+ PUT Object calls fail if the request includes a public ACL\.
+ PUT Bucket calls fail if the request includes a public ACL\.
Enabling this setting doesn't affect existing policies or ACLs\.  
This property is not supported for Amazon S3 on Outposts\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BlockPublicPolicy`  <a name="cfn-s3objectlambda-accesspoint-publicaccessblockconfiguration-blockpublicpolicy"></a>
Specifies whether Amazon S3 should block public bucket policies for buckets in this account\. Setting this element to `TRUE` causes Amazon S3 to reject calls to PUT Bucket policy if the specified bucket policy allows public access\.   
Enabling this setting doesn't affect existing bucket policies\.  
This property is not supported for Amazon S3 on Outposts\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IgnorePublicAcls`  <a name="cfn-s3objectlambda-accesspoint-publicaccessblockconfiguration-ignorepublicacls"></a>
Specifies whether Amazon S3 should ignore public ACLs for buckets in this account\. Setting this element to `TRUE` causes Amazon S3 to ignore all public ACLs on buckets in this account and any objects that they contain\.   
Enabling this setting doesn't affect the persistence of any existing ACLs and doesn't prevent new public ACLs from being set\.  
This property is not supported for Amazon S3 on Outposts\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestrictPublicBuckets`  <a name="cfn-s3objectlambda-accesspoint-publicaccessblockconfiguration-restrictpublicbuckets"></a>
Specifies whether Amazon S3 should restrict public bucket policies for buckets in this account\. Setting this element to `TRUE` restricts access to buckets with public policies to only AWS service principals and authorized users within this account\.  
Enabling this setting doesn't affect previously stored bucket policies, except that public and cross\-account access within any public bucket policy, including non\-public delegation to specific accounts, is blocked\.  
This property is not supported for Amazon S3 on Outposts\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)