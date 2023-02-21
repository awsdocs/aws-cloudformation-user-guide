# AWS::IoT::JobTemplate<a name="aws-resource-iot-jobtemplate"></a>

Represents a job template\.

## Syntax<a name="aws-resource-iot-jobtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-jobtemplate-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::JobTemplate",
  "Properties" : {
      "[AbortConfig](#cfn-iot-jobtemplate-abortconfig)" : AbortConfig,
      "[Description](#cfn-iot-jobtemplate-description)" : String,
      "[Document](#cfn-iot-jobtemplate-document)" : String,
      "[DocumentSource](#cfn-iot-jobtemplate-documentsource)" : String,
      "[JobArn](#cfn-iot-jobtemplate-jobarn)" : String,
      "[JobExecutionsRetryConfig](#cfn-iot-jobtemplate-jobexecutionsretryconfig)" : JobExecutionsRetryConfig,
      "[JobExecutionsRolloutConfig](#cfn-iot-jobtemplate-jobexecutionsrolloutconfig)" : JobExecutionsRolloutConfig,
      "[JobTemplateId](#cfn-iot-jobtemplate-jobtemplateid)" : String,
      "[PresignedUrlConfig](#cfn-iot-jobtemplate-presignedurlconfig)" : PresignedUrlConfig,
      "[Tags](#cfn-iot-jobtemplate-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TimeoutConfig](#cfn-iot-jobtemplate-timeoutconfig)" : TimeoutConfig
    }
}
```

### YAML<a name="aws-resource-iot-jobtemplate-syntax.yaml"></a>

```
Type: AWS::IoT::JobTemplate
Properties: 
  [AbortConfig](#cfn-iot-jobtemplate-abortconfig): 
    AbortConfig
  [Description](#cfn-iot-jobtemplate-description): String
  [Document](#cfn-iot-jobtemplate-document): String
  [DocumentSource](#cfn-iot-jobtemplate-documentsource): String
  [JobArn](#cfn-iot-jobtemplate-jobarn): String
  [JobExecutionsRetryConfig](#cfn-iot-jobtemplate-jobexecutionsretryconfig): 
    JobExecutionsRetryConfig
  [JobExecutionsRolloutConfig](#cfn-iot-jobtemplate-jobexecutionsrolloutconfig): 
    JobExecutionsRolloutConfig
  [JobTemplateId](#cfn-iot-jobtemplate-jobtemplateid): String
  [PresignedUrlConfig](#cfn-iot-jobtemplate-presignedurlconfig): 
    PresignedUrlConfig
  [Tags](#cfn-iot-jobtemplate-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TimeoutConfig](#cfn-iot-jobtemplate-timeoutconfig): 
    TimeoutConfig
```

## Properties<a name="aws-resource-iot-jobtemplate-properties"></a>

`AbortConfig`  <a name="cfn-iot-jobtemplate-abortconfig"></a>
The criteria that determine when and how a job abort takes place\.  
*Required*: No  
*Type*: [AbortConfig](aws-properties-iot-jobtemplate-abortconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-iot-jobtemplate-description"></a>
A description of the job template\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Document`  <a name="cfn-iot-jobtemplate-document"></a>
The job document\.  
Required if you don't specify a value for `documentSource`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DocumentSource`  <a name="cfn-iot-jobtemplate-documentsource"></a>
An S3 link to the job document to use in the template\. Required if you don't specify a value for `document`\.  
If the job document resides in an S3 bucket, you must use a placeholder link when specifying the document\.  
The placeholder link is of the following form:  
 `${aws:iot:s3-presigned-url:https://s3.amazonaws.com/bucket/key}`   
where *bucket* is your bucket name and *key* is the object in the bucket to which you are linking\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`JobArn`  <a name="cfn-iot-jobtemplate-jobarn"></a>
The ARN of the job to use as the basis for the job template\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`JobExecutionsRetryConfig`  <a name="cfn-iot-jobtemplate-jobexecutionsretryconfig"></a>
Allows you to create the criteria to retry a job\.  
*Required*: No  
*Type*: [JobExecutionsRetryConfig](aws-properties-iot-jobtemplate-jobexecutionsretryconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobExecutionsRolloutConfig`  <a name="cfn-iot-jobtemplate-jobexecutionsrolloutconfig"></a>
Allows you to create a staged rollout of a job\.  
*Required*: No  
*Type*: [JobExecutionsRolloutConfig](aws-properties-iot-jobtemplate-jobexecutionsrolloutconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`JobTemplateId`  <a name="cfn-iot-jobtemplate-jobtemplateid"></a>
A unique identifier for the job template\. We recommend using a UUID\. Alpha\-numeric characters, "\-", and "\_" are valid for use here\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PresignedUrlConfig`  <a name="cfn-iot-jobtemplate-presignedurlconfig"></a>
Configuration for pre\-signed S3 URLs\.  
*Required*: No  
*Type*: [PresignedUrlConfig](aws-properties-iot-jobtemplate-presignedurlconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iot-jobtemplate-tags"></a>
Metadata that can be used to manage the job template\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TimeoutConfig`  <a name="cfn-iot-jobtemplate-timeoutconfig"></a>
Specifies the amount of time each device has to finish its execution of the job\. A timer is started when the job execution status is set to `IN_PROGRESS`\. If the job execution status is not set to another terminal state before the timer expires, it will be automatically set to `TIMED_OUT`\.   
*Required*: No  
*Type*: [TimeoutConfig](aws-properties-iot-jobtemplate-timeoutconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iot-jobtemplate-return-values"></a>

### Ref<a name="aws-resource-iot-jobtemplate-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the job template Id\. For example:

 `{ "Ref": "MyJobTemplate-12345" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iot-jobtemplate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-jobtemplate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the job to use as the basis for the job template\.