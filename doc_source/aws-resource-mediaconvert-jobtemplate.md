# AWS::MediaConvert::JobTemplate<a name="aws-resource-mediaconvert-jobtemplate"></a>

The AWS::MediaConvert::JobTemplate resource is an AWS Elemental MediaConvert resource type that you can use to generate transcoding jobs\. 

When you declare this entity in your AWS CloudFormation template, you pass in your transcoding job settings in JSON or YAML format\. This settings specification must be formed in a particular way that conforms to AWS Elemental MediaConvert job validation\. For more information about creating a job template model for the `SettingsJson` property, see the Remarks section later in this topic\.

For information about job templates, see [Working with AWS Elemental MediaConvert Job Templates](https://docs.aws.amazon.com/mediaconvert/latest/ug/working-with-job-templates.html) in the *AWS Elemental MediaConvert User Guide*\.

## Syntax<a name="aws-resource-mediaconvert-jobtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediaconvert-jobtemplate-syntax.json"></a>

```
{
  "Type" : "AWS::MediaConvert::JobTemplate",
  "Properties" : {
      "[AccelerationSettings](#cfn-mediaconvert-jobtemplate-accelerationsettings)" : AccelerationSettings,
      "[Category](#cfn-mediaconvert-jobtemplate-category)" : String,
      "[Description](#cfn-mediaconvert-jobtemplate-description)" : String,
      "[HopDestinations](#cfn-mediaconvert-jobtemplate-hopdestinations)" : [ HopDestination, ... ],
      "[Name](#cfn-mediaconvert-jobtemplate-name)" : String,
      "[Priority](#cfn-mediaconvert-jobtemplate-priority)" : Integer,
      "[Queue](#cfn-mediaconvert-jobtemplate-queue)" : String,
      "[SettingsJson](#cfn-mediaconvert-jobtemplate-settingsjson)" : Json,
      "[StatusUpdateInterval](#cfn-mediaconvert-jobtemplate-statusupdateinterval)" : String,
      "[Tags](#cfn-mediaconvert-jobtemplate-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-mediaconvert-jobtemplate-syntax.yaml"></a>

```
Type: AWS::MediaConvert::JobTemplate
Properties: 
  [AccelerationSettings](#cfn-mediaconvert-jobtemplate-accelerationsettings): 
    AccelerationSettings
  [Category](#cfn-mediaconvert-jobtemplate-category): String
  [Description](#cfn-mediaconvert-jobtemplate-description): String
  [HopDestinations](#cfn-mediaconvert-jobtemplate-hopdestinations): 
    - HopDestination
  [Name](#cfn-mediaconvert-jobtemplate-name): String
  [Priority](#cfn-mediaconvert-jobtemplate-priority): Integer
  [Queue](#cfn-mediaconvert-jobtemplate-queue): String
  [SettingsJson](#cfn-mediaconvert-jobtemplate-settingsjson): 
    Json
  [StatusUpdateInterval](#cfn-mediaconvert-jobtemplate-statusupdateinterval): String
  [Tags](#cfn-mediaconvert-jobtemplate-tags): Json
```

## Properties<a name="aws-resource-mediaconvert-jobtemplate-properties"></a>

`AccelerationSettings`  <a name="cfn-mediaconvert-jobtemplate-accelerationsettings"></a>
Accelerated transcoding can significantly speed up jobs with long, visually complex content\. Outputs that use this feature incur pro\-tier pricing\. For information about feature limitations, For more information, see [Job Limitations for Accelerated Transcoding in AWS Elemental MediaConvert](https://docs.aws.amazon.com/mediaconvert/latest/ug/job-requirements.html) in the *AWS Elemental MediaConvert User Guide*\.  
*Required*: No  
*Type*: [AccelerationSettings](aws-properties-mediaconvert-jobtemplate-accelerationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Category`  <a name="cfn-mediaconvert-jobtemplate-category"></a>
Optional\. A category for the job template you are creating  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-mediaconvert-jobtemplate-description"></a>
Optional\. A description of the job template you are creating\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HopDestinations`  <a name="cfn-mediaconvert-jobtemplate-hopdestinations"></a>
Optional\. Configuration for a destination queue to which the job can hop once a customer\-defined minimum wait time has passed\. For more information, see [Setting Up Queue Hopping to Avoid Long Waits](https://docs.aws.amazon.com/mediaconvert/latest/ug/setting-up-queue-hopping-to-avoid-long-waits.html) in the *AWS Elemental MediaConvert User Guide*\.  
*Required*: No  
*Type*: List of [HopDestination](aws-properties-mediaconvert-jobtemplate-hopdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mediaconvert-jobtemplate-name"></a>
The name of the job template you are creating\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Priority`  <a name="cfn-mediaconvert-jobtemplate-priority"></a>
Specify the relative priority for this job\. In any given queue, the service begins processing the job with the highest value first\. When more than one job has the same priority, the service begins processing the job that you submitted first\. If you don't specify a priority, the service uses the default value 0\. Minimum: \-50 Maximum: 50  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Queue`  <a name="cfn-mediaconvert-jobtemplate-queue"></a>
Optional\. The queue that jobs created from this template are assigned to\. Specify the Amazon Resource Name \(ARN\) of the queue\. For example, arn:aws:mediaconvert:us\-west\-2:505474453218:queues/Default\. If you don't specify this, jobs will go to the default queue\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SettingsJson`  <a name="cfn-mediaconvert-jobtemplate-settingsjson"></a>
Specify, in JSON format, the transcoding job settings for this job template\. This specification must conform to the AWS Elemental MediaConvert job validation\. For information about forming this specification, see the Remarks section later in this topic\.   
For more information about MediaConvert job templates, see [Working with AWS Elemental MediaConvert Job Templates](https://docs.aws.amazon.com/mediaconvert/latest/ug/working-with-job-templates.html) in the *AWS Elemental MediaConvert User Guide*\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatusUpdateInterval`  <a name="cfn-mediaconvert-jobtemplate-statusupdateinterval"></a>
Specify how often MediaConvert sends STATUS\_UPDATE events to Amazon CloudWatch Events\. Set the interval, in seconds, between status updates\. MediaConvert sends an update at this interval from the time the service begins processing your job to the time it completes the transcode or encounters an error\.  
Specify one of the following enums:  
SECONDS\_10  
SECONDS\_12  
SECONDS\_15  
SECONDS\_20  
SECONDS\_30  
SECONDS\_60  
SECONDS\_120  
SECONDS\_180  
SECONDS\_240  
SECONDS\_300  
SECONDS\_360  
SECONDS\_420  
SECONDS\_480  
SECONDS\_540  
SECONDS\_600  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-mediaconvert-jobtemplate-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediaconvert-jobtemplate-return-values"></a>

### Ref<a name="aws-resource-mediaconvert-jobtemplate-return-values-ref"></a>

When you pass the logical ID of an `AWS::MediaConvert::JobTemplate` resource to the intrinsic `Ref` function, the function returns the name of the job template, such as `Streaming stack DASH`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-mediaconvert-jobtemplate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-mediaconvert-jobtemplate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the job template, such as `arn:aws:mediaconvert:us-west-2:123456789012`\.

`Name`  <a name="Name-fn::getatt"></a>
The name of the job template, such as `Streaming stack DASH`\.

## Remarks<a name="aws-resource-mediaconvert-jobtemplate--remarks"></a>

 *Creating a Job Template Model for the SettingsJson Property* 

When you declare an AWS::MediaConvert::JobTemplate entity in your AWS CloudFormation template, you pass in your transcoding job settings as the value for the property `SettingsJson`\. This settings specification must be in in JSON or YAML format and must conform to AWS Elemental MediaConvert job validation\.

The following procedure is for generating the specification in JSON\. If you need it in YAML, you can create it in JSON and use a conversion utility\.

**To create a JSON job template model for `SettingsJson`**

1. Create a job template using the MediaConvert [https://console\.aws\.amazon\.com/mediaconvert/](https://console.aws.amazon.com/mediaconvert/)\. For more information, see [Working with AWS Elemental MediaConvert Job Templates](https://docs.aws.amazon.com/mediaconvert/latest/ug/working-with-job-templates.html)\.

1. Use the AWS CLI to get just the settings structure using the following command:

   `aws mediaconvert https://abcd1234.mediaconvert.region-name-1.amazonaws.com get-job-template DASH-stack-template --query 'JobTemplate.Settings'`

1. Copy the settings as the value for the property `SettingsJson`\.

For an example job template model in JSON and YAML, see the Examples section of this topic\.

## Examples<a name="aws-resource-mediaconvert-jobtemplate--examples"></a>



### Job Template Model for SettingsJson<a name="aws-resource-mediaconvert-jobtemplate--examples--Job_Template_Model_for_SettingsJson"></a>

For more information about creating a job template model in JSON or YAML for the `SettingsJson` property, see the Remarks section of this topic\.

#### JSON<a name="aws-resource-mediaconvert-jobtemplate--examples--Job_Template_Model_for_SettingsJson--json"></a>

```
{
    "AdAvailOffset": 0,
    "OutputGroups": [
        {
            "Name": "File Group",
            "OutputGroupSettings": {
                "FileGroupSettings": {},
                "Type": "FILE_GROUP_SETTINGS"
            },
            "Outputs": [
                {
                    "Extension": "mp4",
                    "NameModifier": "_Generic_Uhd_Mp4_Hevc_Aac_16x9_3840x2160p_24Hz_8Mbps",
                    "Preset": "System-Generic_Uhd_Mp4_Hevc_Aac_16x9_3840x2160p_24Hz_8Mbps"
                },
                {
                    "Extension": "mp4",
                    "NameModifier": "_Generic_Hd_Mp4_Hevc_Aac_16x9_1920x1080p_24Hz_4.5Mbps",
                    "Preset": "System-Generic_Hd_Mp4_Hevc_Aac_16x9_1920x1080p_24Hz_4.5Mbps"
                },
                {
                    "Extension": "mp4",
                    "NameModifier": "_Generic_Hd_Mp4_Hevc_Aac_16x9_1280x720p_24Hz_3.0Mbps",
                    "Preset": "System-Generic_Hd_Mp4_Hevc_Aac_16x9_1280x720p_24Hz_3.0Mbps"
                },
                {
                    "Extension": "mp4",
                    "NameModifier": "_Generic_Hd_Mp4_Avc_Aac_16x9_1920x1080p_24Hz_6Mbps",
                    "Preset": "System-Generic_Hd_Mp4_Avc_Aac_16x9_1920x1080p_24Hz_6Mbps"
                },
                {
                    "Extension": "mp4",
                    "NameModifier": "_Generic_Hd_Mp4_Avc_Aac_16x9_1280x720p_24Hz_4.5Mbps",
                    "Preset": "System-Generic_Hd_Mp4_Avc_Aac_16x9_1280x720p_24Hz_4.5Mbps"
                },
                {
                    "Extension": "mp4",
                    "NameModifier": "_Generic_Sd_Mp4_Avc_Aac_4x3_640x480p_24Hz_1.5Mbps",
                    "Preset": "System-Generic_Sd_Mp4_Avc_Aac_4x3_640x480p_24Hz_1.5Mbps"
                }
            ]
        }
    ]
}
```

#### YAML<a name="aws-resource-mediaconvert-jobtemplate--examples--Job_Template_Model_for_SettingsJson--yaml"></a>

```
---
AdAvailOffset: 0
OutputGroups:
- Name: File Group
  OutputGroupSettings:
    FileGroupSettings: {}
    Type: FILE_GROUP_SETTINGS
  Outputs:
  - Extension: mp4
    NameModifier: _Generic_Uhd_Mp4_Hevc_Aac_16x9_3840x2160p_24Hz_8Mbps
    Preset: System-Generic_Uhd_Mp4_Hevc_Aac_16x9_3840x2160p_24Hz_8Mbps
  - Extension: mp4
    NameModifier: _Generic_Hd_Mp4_Hevc_Aac_16x9_1920x1080p_24Hz_4.5Mbps
    Preset: System-Generic_Hd_Mp4_Hevc_Aac_16x9_1920x1080p_24Hz_4.5Mbps
  - Extension: mp4
    NameModifier: _Generic_Hd_Mp4_Hevc_Aac_16x9_1280x720p_24Hz_3.0Mbps
    Preset: System-Generic_Hd_Mp4_Hevc_Aac_16x9_1280x720p_24Hz_3.0Mbps
  - Extension: mp4
    NameModifier: _Generic_Hd_Mp4_Avc_Aac_16x9_1920x1080p_24Hz_6Mbps
    Preset: System-Generic_Hd_Mp4_Avc_Aac_16x9_1920x1080p_24Hz_6Mbps
  - Extension: mp4
    NameModifier: _Generic_Hd_Mp4_Avc_Aac_16x9_1280x720p_24Hz_4.5Mbps
    Preset: System-Generic_Hd_Mp4_Avc_Aac_16x9_1280x720p_24Hz_4.5Mbps
  - Extension: mp4
    NameModifier: _Generic_Sd_Mp4_Avc_Aac_4x3_640x480p_24Hz_1.5Mbps
    Preset: System-Generic_Sd_Mp4_Avc_Aac_4x3_640x480p_24Hz_1.5Mbps
```