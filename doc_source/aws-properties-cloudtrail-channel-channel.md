# AWS::CloudTrail::Channel Channel<a name="aws-properties-cloudtrail-channel-channel"></a>

Contains information about a returned CloudTrail channel\.

## Syntax<a name="aws-properties-cloudtrail-channel-channel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudtrail-channel-channel-syntax.json"></a>

```
{
  "[ChannelArn](#cfn-cloudtrail-channel-channel-channelarn)" : String,
  "[Name](#cfn-cloudtrail-channel-channel-name)" : String
}
```

### YAML<a name="aws-properties-cloudtrail-channel-channel-syntax.yaml"></a>

```
  [ChannelArn](#cfn-cloudtrail-channel-channel-channelarn): String
  [Name](#cfn-cloudtrail-channel-channel-name): String
```

## Properties<a name="aws-properties-cloudtrail-channel-channel-properties"></a>

`ChannelArn`  <a name="cfn-cloudtrail-channel-channel-channelarn"></a>
The Amazon Resource Name \(ARN\) of a channel\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `256`  
*Pattern*: `^[a-zA-Z0-9._/\-:]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudtrail-channel-channel-name"></a>
 The name of the CloudTrail channel\. For service\-linked channels, the name is `aws-service-channel/service-name/custom-suffix` where `service-name` represents the name of the AWS service that created the channel and `custom-suffix` represents the suffix created by the AWS service\.   
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9._\-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)