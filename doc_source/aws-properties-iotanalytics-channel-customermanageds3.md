# AWS::IoTAnalytics::Channel CustomerManagedS3<a name="aws-properties-iotanalytics-channel-customermanageds3"></a>

Use this to store channel data in an S3 bucket that you manage\. When customer managed storage is selected, the "retentionPeriod" parameter is ignored\. The choice of service\-managed or customer\-managed S3 storage cannot be changed after creation of the channel\.

## Syntax<a name="aws-properties-iotanalytics-channel-customermanageds3-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-channel-customermanageds3-syntax.json"></a>

```
{
  "[Bucket](#cfn-iotanalytics-channel-customermanageds3-bucket)" : String,
  "[KeyPrefix](#cfn-iotanalytics-channel-customermanageds3-keyprefix)" : String,
  "[RoleArn](#cfn-iotanalytics-channel-customermanageds3-rolearn)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-channel-customermanageds3-syntax.yaml"></a>

```
  [Bucket](#cfn-iotanalytics-channel-customermanageds3-bucket): String
  [KeyPrefix](#cfn-iotanalytics-channel-customermanageds3-keyprefix): String
  [RoleArn](#cfn-iotanalytics-channel-customermanageds3-rolearn): String
```

## Properties<a name="aws-properties-iotanalytics-channel-customermanageds3-properties"></a>

`Bucket`  <a name="cfn-iotanalytics-channel-customermanageds3-bucket"></a>
The name of the Amazon S3 bucket in which channel data is stored\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyPrefix`  <a name="cfn-iotanalytics-channel-customermanageds3-keyprefix"></a>
\[Optional\] The prefix used to create the keys of the channel data objects\. Each object in an Amazon S3 bucket has a key that is its unique identifier within the bucket \(each object in a bucket has exactly one key\)\. The prefix must end with a '/'\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iotanalytics-channel-customermanageds3-rolearn"></a>
The ARN of the role which grants AWS IoT Analytics permission to interact with your Amazon S3 resources\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)