# AWS::MediaLive::Channel FrameCaptureGroupSettings<a name="aws-properties-medialive-channel-framecapturegroupsettings"></a>

The settings for a frame capture output group\.

The parent of this entity is OutputGroupSettings\.

## Syntax<a name="aws-properties-medialive-channel-framecapturegroupsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-framecapturegroupsettings-syntax.json"></a>

```
{
  "[Destination](#cfn-medialive-channel-framecapturegroupsettings-destination)" : OutputLocationRef
}
```

### YAML<a name="aws-properties-medialive-channel-framecapturegroupsettings-syntax.yaml"></a>

```
  [Destination](#cfn-medialive-channel-framecapturegroupsettings-destination): 
    OutputLocationRef
```

## Properties<a name="aws-properties-medialive-channel-framecapturegroupsettings-properties"></a>

`Destination`  <a name="cfn-medialive-channel-framecapturegroupsettings-destination"></a>
The destination for the frame capture files\. The destination is either the URI for an Amazon S3 bucket and object, plus a file name prefix \(for example, s3ssl://sportsDelivery/highlights/20180820/curling\_\) or the URI for a MediaStore container, plus a file name prefix \(for example, mediastoressl://sportsDelivery/20180820/curling\_\)\. The final file names consist of the prefix from the destination field \(for example, "curling\_"\) \+ name modifier \+ the counter \(5 digits, starting from 00001\) \+ extension \(which is always \.jpg\)\. For example, curlingLow\.00001\.jpg\.  
*Required*: No  
*Type*: [OutputLocationRef](aws-properties-medialive-channel-outputlocationref.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)