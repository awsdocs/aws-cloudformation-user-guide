# AWS::KafkaConnect::Connector S3LogDelivery<a name="aws-properties-kafkaconnect-connector-s3logdelivery"></a>

Details about delivering logs to Amazon S3\.

## Syntax<a name="aws-properties-kafkaconnect-connector-s3logdelivery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-s3logdelivery-syntax.json"></a>

```
{
  "[Bucket](#cfn-kafkaconnect-connector-s3logdelivery-bucket)" : String,
  "[Enabled](#cfn-kafkaconnect-connector-s3logdelivery-enabled)" : Boolean,
  "[Prefix](#cfn-kafkaconnect-connector-s3logdelivery-prefix)" : String
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-s3logdelivery-syntax.yaml"></a>

```
  [Bucket](#cfn-kafkaconnect-connector-s3logdelivery-bucket): String
  [Enabled](#cfn-kafkaconnect-connector-s3logdelivery-enabled): Boolean
  [Prefix](#cfn-kafkaconnect-connector-s3logdelivery-prefix): String
```

## Properties<a name="aws-properties-kafkaconnect-connector-s3logdelivery-properties"></a>

`Bucket`  <a name="cfn-kafkaconnect-connector-s3logdelivery-bucket"></a>
The name of the S3 bucket that is the destination for log delivery\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Enabled`  <a name="cfn-kafkaconnect-connector-s3logdelivery-enabled"></a>
Specifies whether connector logs get sent to the specified Amazon S3 destination\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Prefix`  <a name="cfn-kafkaconnect-connector-s3logdelivery-prefix"></a>
The S3 prefix that is the destination for log delivery\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)