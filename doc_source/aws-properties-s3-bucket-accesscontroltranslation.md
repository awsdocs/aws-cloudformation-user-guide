# AWS::S3::Bucket AccessControlTranslation<a name="aws-properties-s3-bucket-accesscontroltranslation"></a>

Specify this only in a cross\-account scenario \(where source and destination bucket owners are not the same\), and you want to change replica ownership to the AWS account that owns the destination bucket\. If this is not specified in the replication configuration, the replicas are owned by same AWS account that owns the source object\.

## Syntax<a name="aws-properties-s3-bucket-accesscontroltranslation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-accesscontroltranslation-syntax.json"></a>

```
{
  "[Owner](#cfn-s3-bucket-accesscontroltranslation-owner)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-accesscontroltranslation-syntax.yaml"></a>

```
  [Owner](#cfn-s3-bucket-accesscontroltranslation-owner): String
```

## Properties<a name="aws-properties-s3-bucket-accesscontroltranslation-properties"></a>

`Owner`  <a name="cfn-s3-bucket-accesscontroltranslation-owner"></a>
Specifies the replica ownership\. For default and valid values, see [PUT bucket replication](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTreplication.html) in the *Amazon Simple Storage Service API Reference*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Destination`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)