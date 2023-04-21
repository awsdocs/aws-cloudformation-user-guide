# AWS::IoT::JobTemplate PresignedUrlConfig<a name="aws-properties-iot-jobtemplate-presignedurlconfig"></a>

Configuration for pre\-signed S3 URLs\.

## Syntax<a name="aws-properties-iot-jobtemplate-presignedurlconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-jobtemplate-presignedurlconfig-syntax.json"></a>

```
{
  "[ExpiresInSec](#cfn-iot-jobtemplate-presignedurlconfig-expiresinsec)" : Integer,
  "[RoleArn](#cfn-iot-jobtemplate-presignedurlconfig-rolearn)" : String
}
```

### YAML<a name="aws-properties-iot-jobtemplate-presignedurlconfig-syntax.yaml"></a>

```
  [ExpiresInSec](#cfn-iot-jobtemplate-presignedurlconfig-expiresinsec): Integer
  [RoleArn](#cfn-iot-jobtemplate-presignedurlconfig-rolearn): String
```

## Properties<a name="aws-properties-iot-jobtemplate-presignedurlconfig-properties"></a>

`ExpiresInSec`  <a name="cfn-iot-jobtemplate-presignedurlconfig-expiresinsec"></a>
How long \(in seconds\) pre\-signed URLs are valid\. Valid values are 60 \- 3600, the default value is 3600 seconds\. Pre\-signed URLs are generated when Jobs receives an MQTT request for the job document\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-iot-jobtemplate-presignedurlconfig-rolearn"></a>
The ARN of an IAM role that grants grants permission to download files from the S3 bucket where the job data/updates are stored\. The role must also grant permission for IoT to download the files\.  
For information about addressing the confused deputy problem, see [cross\-service confused deputy prevention](https://docs.aws.amazon.com/iot/latest/developerguide/cross-service-confused-deputy-prevention.html) in the * AWS IoT Core developer guide*\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)