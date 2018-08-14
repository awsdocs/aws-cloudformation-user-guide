# AWS IoT TopicRule S3Action<a name="aws-properties-iot-topicrule-s3action"></a>

`S3` is a property of the `Actions` property that describes an action that writes data to an S3 bucket\.

## Syntax<a name="w3ab2c21c14e1370b5"></a>

### JSON<a name="aws-properties-iot-topicrule-s3action-syntax.json"></a>

```
{
  "[BucketName](#cfn-iot-topicrule-s3action-bucketname)": String,
  "[Key](#cfn-iot-topicrule-s3action-key)": String,
  "[RoleArn](#cfn-iot-topicrule-s3action-rolearn)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-s3action-syntax.yaml"></a>

```
[BucketName](#cfn-iot-topicrule-s3action-bucketname): String
[Key](#cfn-iot-topicrule-s3action-key): String
[RoleArn](#cfn-iot-topicrule-s3action-rolearn): String
```

## Properties<a name="w3ab2c21c14e1370b7"></a>

`BucketName`  <a name="cfn-iot-topicrule-s3action-bucketname"></a>
The name of the S3 bucket\.  
*Required*: Yes  
*Type*: String

`Key`  <a name="cfn-iot-topicrule-s3action-key"></a>
The object key \(the name of an object in the S3 bucket\)\.  
*Required*: Yes  
*Type*: String

`RoleArn`  <a name="cfn-iot-topicrule-s3action-rolearn"></a>
The ARN of the IAM role that grants access to Amazon S3\.  
*Required*: Yes  
*Type*: String