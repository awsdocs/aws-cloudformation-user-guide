# AWS::IoT::TopicRule S3Action<a name="aws-properties-iot-topicrule-s3action"></a>

Describes an action to write data to an Amazon S3 bucket\.

## Syntax<a name="aws-properties-iot-topicrule-s3action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-s3action-syntax.json"></a>

```
{
  "[BucketName](#cfn-iot-topicrule-s3action-bucketname)" : String,
  "[Key](#cfn-iot-topicrule-s3action-key)" : String,
  "[RoleArn](#cfn-iot-topicrule-s3action-rolearn)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-s3action-syntax.yaml"></a>

```
  [BucketName](#cfn-iot-topicrule-s3action-bucketname): String
  [Key](#cfn-iot-topicrule-s3action-key): String
  [RoleArn](#cfn-iot-topicrule-s3action-rolearn): String
```

## Properties<a name="aws-properties-iot-topicrule-s3action-properties"></a>

`BucketName`  <a name="cfn-iot-topicrule-s3action-bucketname"></a>
The Amazon S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-iot-topicrule-s3action-key"></a>
The object key\. For more information, see [Actions, resources, and condition keys for Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/dev/list_amazons3.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-s3action-rolearn"></a>
The ARN of the IAM role that grants access\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)