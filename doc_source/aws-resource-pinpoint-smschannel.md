# AWS::Pinpoint::SMSChannel<a name="aws-resource-pinpoint-smschannel"></a>

A *channel* is a type of platform that you can deliver messages to\. To send an SMS text message, you send the message through the SMS channel\. Before you can use Amazon Pinpoint to send text messages, you have to enable the SMS channel for an Amazon Pinpoint application\.

The AWS::Pinpoint::SMSChannel resource defines the status, sender ID, and other settings of the SMS channel for an application\.

## Syntax<a name="aws-resource-pinpoint-smschannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-smschannel-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::SMSChannel",
  "Properties" : {
      "[ApplicationId](#cfn-pinpoint-smschannel-applicationid)" : String,
      "[Enabled](#cfn-pinpoint-smschannel-enabled)" : Boolean,
      "[SenderId](#cfn-pinpoint-smschannel-senderid)" : String,
      "[ShortCode](#cfn-pinpoint-smschannel-shortcode)" : String
    }
}
```

### YAML<a name="aws-resource-pinpoint-smschannel-syntax.yaml"></a>

```
Type: AWS::Pinpoint::SMSChannel
Properties: 
  [ApplicationId](#cfn-pinpoint-smschannel-applicationid): String
  [Enabled](#cfn-pinpoint-smschannel-enabled): Boolean
  [SenderId](#cfn-pinpoint-smschannel-senderid): String
  [ShortCode](#cfn-pinpoint-smschannel-shortcode): String
```

## Properties<a name="aws-resource-pinpoint-smschannel-properties"></a>

`ApplicationId`  <a name="cfn-pinpoint-smschannel-applicationid"></a>
The unique identifier for the application that the SMS channel applies to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Enabled`  <a name="cfn-pinpoint-smschannel-enabled"></a>
Specifies whether to enable the SMS channel for the application\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SenderId`  <a name="cfn-pinpoint-smschannel-senderid"></a>
The identity that you want to display on recipients' devices when they receive messages from the SMS channel\.  
SenderIDs are only supported in certain countries and regions\. For more information, see [Supported Countries and Regions](https://docs.aws.amazon.com/pinpoint/latest/userguide/channels-sms-countries.html) in the *Amazon Pinpoint User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShortCode`  <a name="cfn-pinpoint-smschannel-shortcode"></a>
The registered short code that you want to use when you send messages through the SMS channel\.  
For information about obtaining a dedicated short code for sending SMS messages, see [Requesting Dedicated Short Codes for SMS Messaging](https://docs.aws.amazon.com/pinpoint/latest/userguide/channels-sms-awssupport-short-code.html) in the *Amazon Pinpoint User Guide*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpoint-smschannel-return-values"></a>

### Ref<a name="aws-resource-pinpoint-smschannel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier \(`ApplicationId`\) for the Amazon Pinpoint application that the channel is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.