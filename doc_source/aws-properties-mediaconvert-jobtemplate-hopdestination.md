# AWS::MediaConvert::JobTemplate HopDestination<a name="aws-properties-mediaconvert-jobtemplate-hopdestination"></a>

Optional\. Configuration for a destination queue to which the job can hop once a customer\-defined minimum wait time has passed\. For more information, see [Setting Up Queue Hopping to Avoid Long Waits](https://docs.aws.amazon.com/mediaconvert/latest/ug/setting-up-queue-hopping-to-avoid-long-waits.html) in the *AWS Elemental MediaConvert User Guide*\.

## Syntax<a name="aws-properties-mediaconvert-jobtemplate-hopdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconvert-jobtemplate-hopdestination-syntax.json"></a>

```
{
  "[Priority](#cfn-mediaconvert-jobtemplate-hopdestination-priority)" : Integer,
  "[Queue](#cfn-mediaconvert-jobtemplate-hopdestination-queue)" : String,
  "[WaitMinutes](#cfn-mediaconvert-jobtemplate-hopdestination-waitminutes)" : Integer
}
```

### YAML<a name="aws-properties-mediaconvert-jobtemplate-hopdestination-syntax.yaml"></a>

```
  [Priority](#cfn-mediaconvert-jobtemplate-hopdestination-priority): Integer
  [Queue](#cfn-mediaconvert-jobtemplate-hopdestination-queue): String
  [WaitMinutes](#cfn-mediaconvert-jobtemplate-hopdestination-waitminutes): Integer
```

## Properties<a name="aws-properties-mediaconvert-jobtemplate-hopdestination-properties"></a>

`Priority`  <a name="cfn-mediaconvert-jobtemplate-hopdestination-priority"></a>
Optional\. When you set up a job to use queue hopping, you can specify a different relative priority for the job in the destination queue\. If you don't specify, the relative priority will remain the same as in the previous queue\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Queue`  <a name="cfn-mediaconvert-jobtemplate-hopdestination-queue"></a>
Optional unless the job is submitted on the default queue\. When you set up a job to use queue hopping, you can specify a destination queue\. This queue cannot be the original queue to which the job is submitted\. If the original queue isn't the default queue and you don't specify the destination queue, the job will move to the default queue\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaitMinutes`  <a name="cfn-mediaconvert-jobtemplate-hopdestination-waitminutes"></a>
Required for setting up a job to use queue hopping\. Minimum wait time in minutes until the job can hop to the destination queue\. Valid range is 1 to 1440 minutes, inclusive\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)