# AWS::S3::AccessPoint PublicAccessBlockConfiguration<a name="aws-properties-s3-accesspoint-publicaccessblockconfiguration"></a>

The PublicAccessBlock configuration that you want to apply to this Amazon S3 bucket\. You can enable the configuration options in any combination\. For more information about when Amazon S3 considers a bucket or object public, see [The Meaning of "Public"](https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html#access-control-block-public-access-policy-status) in the *Amazon Simple Storage Service Developer Guide*\. 

## Syntax<a name="aws-properties-s3-accesspoint-publicaccessblockconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-accesspoint-publicaccessblockconfiguration-syntax.json"></a>

```
{
  "[BlockPublicAcls](#cfn-s3-accesspoint-publicaccessblockconfiguration-blockpublicacls)" : Boolean,
  "[BlockPublicPolicy](#cfn-s3-accesspoint-publicaccessblockconfiguration-blockpublicpolicy)" : Boolean,
  "[IgnorePublicAcls](#cfn-s3-accesspoint-publicaccessblockconfiguration-ignorepublicacls)" : Boolean,
  "[RestrictPublicBuckets](#cfn-s3-accesspoint-publicaccessblockconfiguration-restrictpublicbuckets)" : Boolean
}
```

### YAML<a name="aws-properties-s3-accesspoint-publicaccessblockconfiguration-syntax.yaml"></a>

```
  [BlockPublicAcls](#cfn-s3-accesspoint-publicaccessblockconfiguration-blockpublicacls): Boolean
  [BlockPublicPolicy](#cfn-s3-accesspoint-publicaccessblockconfiguration-blockpublicpolicy): Boolean
  [IgnorePublicAcls](#cfn-s3-accesspoint-publicaccessblockconfiguration-ignorepublicacls): Boolean
  [RestrictPublicBuckets](#cfn-s3-accesspoint-publicaccessblockconfiguration-restrictpublicbuckets): Boolean
```

## Properties<a name="aws-properties-s3-accesspoint-publicaccessblockconfiguration-properties"></a>

`BlockPublicAcls`  <a name="cfn-s3-accesspoint-publicaccessblockconfiguration-blockpublicacls"></a>
Specifies whether Amazon S3 should block public access control lists \(ACLs\) for this bucket and objects in this bucket\. Setting this element to `TRUE` causes the following behavior:  
+ PUT Bucket acl and PUT Object acl calls fail if the specified ACL is public\.
+ PUT Object calls fail if the request includes a public ACL\.
+ PUT Bucket calls fail if the request includes a public ACL\.
Enabling this setting doesn't affect existing policies or ACLs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BlockPublicPolicy`  <a name="cfn-s3-accesspoint-publicaccessblockconfiguration-blockpublicpolicy"></a>
Specifies whether Amazon S3 should block public bucket policies for this bucket\. Setting this element to `TRUE` causes Amazon S3 to reject calls to PUT Bucket policy if the specified bucket policy allows public access\.   
Enabling this setting doesn't affect existing bucket policies\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IgnorePublicAcls`  <a name="cfn-s3-accesspoint-publicaccessblockconfiguration-ignorepublicacls"></a>
Specifies whether Amazon S3 should ignore public ACLs for this bucket and objects in this bucket\. Setting this element to `TRUE` causes Amazon S3 to ignore all public ACLs on this bucket and objects in this bucket\.  
Enabling this setting doesn't affect the persistence of any existing ACLs and doesn't prevent new public ACLs from being set\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RestrictPublicBuckets`  <a name="cfn-s3-accesspoint-publicaccessblockconfiguration-restrictpublicbuckets"></a>
Specifies whether Amazon S3 should restrict public bucket policies for this bucket\. Setting this element to `TRUE` restricts access to this bucket to only AWS service principals and authorized users within this account if the bucket has a public policy\.  
Enabling this setting doesn't affect previously stored bucket policies, except that public and cross\-account access within any public bucket policy, including non\-public delegation to specific accounts, is blocked\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)