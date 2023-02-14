# AWS::IoTAnalytics::Channel CustomerManagedS3<a name="aws-properties-iotanalytics-channel-customermanageds3"></a>

Used to store channel data in an S3 bucket that you manage\.

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
The name of the S3 bucket in which channel data is stored\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `255`  
*Pattern*: `^[a-zA-Z0-9.\-_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyPrefix`  <a name="cfn-iotanalytics-channel-customermanageds3-keyprefix"></a>
\(Optional\) The prefix used to create the keys of the channel data objects\. Each object in an S3 bucket has a key that is its unique identifier within the bucket \(each object in a bucket has exactly one key\)\. The prefix must end with a forward slash \(/\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[a-zA-Z0-9!_.*'()/{}:-]*/$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iotanalytics-channel-customermanageds3-rolearn"></a>
The ARN of the role that grants AWS IoT Analytics permission to interact with your Amazon S3 resources\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)