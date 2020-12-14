# AWS::MediaConvert::JobTemplate AccelerationSettings<a name="aws-properties-mediaconvert-jobtemplate-accelerationsettings"></a>

Accelerated transcoding can significantly speed up jobs with long, visually complex content\. Outputs that use this feature incur pro\-tier pricing\. For information about feature limitations, For more information, see [Job Limitations for Accelerated Transcoding in AWS Elemental MediaConvert](https://docs.aws.amazon.com/mediaconvert/latest/ug/job-requirements.html) in the *AWS Elemental MediaConvert User Guide*\.

## Syntax<a name="aws-properties-mediaconvert-jobtemplate-accelerationsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconvert-jobtemplate-accelerationsettings-syntax.json"></a>

```
{
  "[Mode](#cfn-mediaconvert-jobtemplate-accelerationsettings-mode)" : String
}
```

### YAML<a name="aws-properties-mediaconvert-jobtemplate-accelerationsettings-syntax.yaml"></a>

```
  [Mode](#cfn-mediaconvert-jobtemplate-accelerationsettings-mode): String
```

## Properties<a name="aws-properties-mediaconvert-jobtemplate-accelerationsettings-properties"></a>

`Mode`  <a name="cfn-mediaconvert-jobtemplate-accelerationsettings-mode"></a>
Specify the conditions when the service will run your job with accelerated transcoding\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)