# Amazon S3 Bucket ServerSideEncryptionRule<a name="aws-properties-s3-bucket-serversideencryptionrule"></a>

The `ServerSideEncryptionRule` property is part of the [AWS::S3::Bucket](aws-properties-s3-bucket.md) resource that specifies the server\-side encryption by default configuration\. For more information, see [PUT Bucket encryption](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTencryption.html) in the *Amazon Simple Storage Service API Reference*\.

## Syntax<a name="w3ab2c21c14e1772b5"></a>

### JSON<a name="aws-properties-s3-bucket-serversideencryptionrule.json"></a>

```
{
  "[ServerSideEncryptionByDefault](#cfn-s3-bucket-serversideencryptionrule-serversideencryptionbydefault)" : [*ServerSideEncryptionByDefault*](aws-properties-s3-bucket-serversideencryptionbydefault.md)
}
```

### YAML<a name="aws-properties-s3-bucket-serversideencryptionrule.yaml"></a>

```
[ServerSideEncryptionByDefault](#cfn-s3-bucket-serversideencryptionrule-serversideencryptionbydefault): 
 [*ServerSideEncryptionByDefault*](aws-properties-s3-bucket-serversideencryptionbydefault.md)
```

## Properties<a name="w3ab2c21c14e1772b7"></a>

`ServerSideEncryptionByDefault`  <a name="cfn-s3-bucket-serversideencryptionrule-serversideencryptionbydefault"></a>
Sets server\-side encryption by default\.  
*Required*: No  
*Type:* [ServerSideEncryptionByDefault](aws-properties-s3-bucket-serversideencryptionbydefault.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)