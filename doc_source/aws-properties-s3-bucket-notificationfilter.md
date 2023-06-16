# AWS::S3::Bucket NotificationFilter<a name="aws-properties-s3-bucket-notificationfilter"></a>

Specifies object key name filtering rules\. For information about key name filtering, see [Configuring event notifications using object key name filtering](https://docs.aws.amazon.com/AmazonS3/latest/userguide/notification-how-to-filtering.html) in the *Amazon S3 User Guide*\.

## Syntax<a name="aws-properties-s3-bucket-notificationfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-notificationfilter-syntax.json"></a>

```
{
  "[S3Key](#cfn-s3-bucket-notificationfilter-s3key)" : S3KeyFilter
}
```

### YAML<a name="aws-properties-s3-bucket-notificationfilter-syntax.yaml"></a>

```
  [S3Key](#cfn-s3-bucket-notificationfilter-s3key): 
    S3KeyFilter
```

## Properties<a name="aws-properties-s3-bucket-notificationfilter-properties"></a>

`S3Key`  <a name="cfn-s3-bucket-notificationfilter-s3key"></a>
A container for object key name prefix and suffix filtering rules\.  
*Required*: Yes  
*Type*: [S3KeyFilter](aws-properties-s3-bucket-s3keyfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)