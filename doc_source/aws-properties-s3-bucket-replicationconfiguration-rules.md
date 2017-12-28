# Amazon S3 Bucket ReplicationRule<a name="aws-properties-s3-bucket-replicationconfiguration-rules"></a>

The `ReplicationRule` property type specifies which Amazon Simple Storage Service \(Amazon S3\) objects to replicate and where to store them\. The `Rules` subproperty of the [Amazon S3 Bucket ReplicationConfiguration](aws-properties-s3-bucket-replicationconfiguration.md) property contains a list of `ReplicationRule` property types\.

## Syntax<a name="w3ab2c21c14e1525b5"></a>

### JSON<a name="aws-properties-s3-bucket-replicationconfiguration-rules-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-replicationconfiguration-rules-destination)" : ReplicationDestination,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-replicationconfiguration-rules-id)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-replicationconfiguration-rules-prefix)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-replicationconfiguration-rules-status)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-replicationconfiguration-rules-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-replicationconfiguration-rules-destination): 
  ReplicationDestination
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-replicationconfiguration-rules-id): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-replicationconfiguration-rules-prefix): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-replicationconfiguration-rules-status): String
```

## Properties<a name="w3ab2c21c14e1525b7"></a>

`Destination`  
Defines the destination where Amazon S3 stores replicated objects\.  
*Required: *Yes  
*Type*: [Amazon S3 Bucket ReplicationDestination](aws-properties-s3-bucket-replicationconfiguration-rules-destination.md)

`Id`  
A unique identifier for the rule\. If you don't specify a value, AWS CloudFormation generates a random ID\.  
*Required: *No  
*Type*: String

`Prefix`  
An object prefix\. This rule applies to all Amazon S3 objects with this prefix\. To specify all objects in an S3 bucket, specify an empty string\.  
*Required: *Yes  
*Type*: String

`Status`  
Whether the rule is enabled\. For valid values, see the `Status` element of the [PUT Bucket replication](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTreplication.html) action in the *Amazon Simple Storage Service API Reference*\.  
*Required: *Yes  
*Type*: String