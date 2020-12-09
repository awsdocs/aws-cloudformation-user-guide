# AWS::Pinpoint::GCMChannel<a name="aws-resource-pinpoint-gcmchannel"></a>

A *channel* is a type of platform that you can deliver messages to\. You can use the GCM channel to send push notification messages to the Firebase Cloud Messaging \(FCM\) service, which replaced the Google Cloud Messaging \(GCM\) service\. Before you use Amazon Pinpoint to send notifications to FCM, you have to enable the GCM channel for an Amazon Pinpoint application\.

The AWS::Pinpoint::GCMChannel resource defines the status and authentication settings of the GCM channel for an application\.

## Syntax<a name="aws-resource-pinpoint-gcmchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-gcmchannel-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::GCMChannel",
  "Properties" : {
      "[ApiKey](#cfn-pinpoint-gcmchannel-apikey)" : String,
      "[ApplicationId](#cfn-pinpoint-gcmchannel-applicationid)" : String,
      "[Enabled](#cfn-pinpoint-gcmchannel-enabled)" : Boolean
    }
}
```

### YAML<a name="aws-resource-pinpoint-gcmchannel-syntax.yaml"></a>

```
Type: AWS::Pinpoint::GCMChannel
Properties: 
  [ApiKey](#cfn-pinpoint-gcmchannel-apikey): String
  [ApplicationId](#cfn-pinpoint-gcmchannel-applicationid): String
  [Enabled](#cfn-pinpoint-gcmchannel-enabled): Boolean
```

## Properties<a name="aws-resource-pinpoint-gcmchannel-properties"></a>

`ApiKey`  <a name="cfn-pinpoint-gcmchannel-apikey"></a>
The Web API Key, also referred to as an *API\_KEY* or *server key*, that you received from Google to communicate with Google services\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApplicationId`  <a name="cfn-pinpoint-gcmchannel-applicationid"></a>
The unique identifier for the application that the GCM channel applies to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Enabled`  <a name="cfn-pinpoint-gcmchannel-enabled"></a>
Specifies whether to enable the GCM channel for the application\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpoint-gcmchannel-return-values"></a>

### Ref<a name="aws-resource-pinpoint-gcmchannel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier \(`ApplicationId`\) for the Amazon Pinpoint application that the channel is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.