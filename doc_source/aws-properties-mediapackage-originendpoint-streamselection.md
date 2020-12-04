# AWS::MediaPackage::OriginEndpoint StreamSelection<a name="aws-properties-mediapackage-originendpoint-streamselection"></a>

Limitations for outputs from the endpoint, based on the video bitrate\. 

## Syntax<a name="aws-properties-mediapackage-originendpoint-streamselection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-originendpoint-streamselection-syntax.json"></a>

```
{
  "[MaxVideoBitsPerSecond](#cfn-mediapackage-originendpoint-streamselection-maxvideobitspersecond)" : Integer,
  "[MinVideoBitsPerSecond](#cfn-mediapackage-originendpoint-streamselection-minvideobitspersecond)" : Integer,
  "[StreamOrder](#cfn-mediapackage-originendpoint-streamselection-streamorder)" : String
}
```

### YAML<a name="aws-properties-mediapackage-originendpoint-streamselection-syntax.yaml"></a>

```
  [MaxVideoBitsPerSecond](#cfn-mediapackage-originendpoint-streamselection-maxvideobitspersecond): Integer
  [MinVideoBitsPerSecond](#cfn-mediapackage-originendpoint-streamselection-minvideobitspersecond): Integer
  [StreamOrder](#cfn-mediapackage-originendpoint-streamselection-streamorder): String
```

## Properties<a name="aws-properties-mediapackage-originendpoint-streamselection-properties"></a>

`MaxVideoBitsPerSecond`  <a name="cfn-mediapackage-originendpoint-streamselection-maxvideobitspersecond"></a>
The upper limit of the bitrates that this endpoint serves\. If the video track exceeds this threshold, then AWS Elemental MediaPackage excludes it from output\. If you don't specify a value, it defaults to 2147483647 bits per second\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinVideoBitsPerSecond`  <a name="cfn-mediapackage-originendpoint-streamselection-minvideobitspersecond"></a>
The lower limit of the bitrates that this endpoint serves\. If the video track is below this threshold, then AWS Elemental MediaPackage excludes it from output\. If you don't specify a value, it defaults to 0 bits per second\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamOrder`  <a name="cfn-mediapackage-originendpoint-streamselection-streamorder"></a>
Order in which the different video bitrates are presented to the player\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)