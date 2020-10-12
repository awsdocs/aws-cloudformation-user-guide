# AWS::Pinpoint::ADMChannel<a name="aws-resource-pinpoint-admchannel"></a>

A *channel* is a type of platform that you can deliver messages to\. You can use the ADM channel to send push notifications through the Amazon Device Messaging \(ADM\) service to apps that run on Amazon devices, such as Kindle Fire tablets\. Before you can use Amazon Pinpoint to send messages to Amazon devices, you have to enable the ADM channel for an Amazon Pinpoint application\.

The AWS::Pinpoint::ADMChannel resource defines the status and authentication settings of the ADM channel for an application\.

## Syntax<a name="aws-resource-pinpoint-admchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-admchannel-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::ADMChannel",
  "Properties" : {
      "[ApplicationId](#cfn-pinpoint-admchannel-applicationid)" : String,
      "[ClientId](#cfn-pinpoint-admchannel-clientid)" : String,
      "[ClientSecret](#cfn-pinpoint-admchannel-clientsecret)" : String,
      "[Enabled](#cfn-pinpoint-admchannel-enabled)" : Boolean
    }
}
```

### YAML<a name="aws-resource-pinpoint-admchannel-syntax.yaml"></a>

```
Type: AWS::Pinpoint::ADMChannel
Properties: 
  [ApplicationId](#cfn-pinpoint-admchannel-applicationid): String
  [ClientId](#cfn-pinpoint-admchannel-clientid): String
  [ClientSecret](#cfn-pinpoint-admchannel-clientsecret): String
  [Enabled](#cfn-pinpoint-admchannel-enabled): Boolean
```

## Properties<a name="aws-resource-pinpoint-admchannel-properties"></a>

`ApplicationId`  <a name="cfn-pinpoint-admchannel-applicationid"></a>
The unique identifier for the application that the ADM channel applies to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClientId`  <a name="cfn-pinpoint-admchannel-clientid"></a>
The Client ID that you received from Amazon to send messages by using ADM\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientSecret`  <a name="cfn-pinpoint-admchannel-clientsecret"></a>
The Client Secret that you received from Amazon to send messages by using ADM\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-pinpoint-admchannel-enabled"></a>
Specifies whether to enable the ADM channel for the application\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpoint-admchannel-return-values"></a>

### Ref<a name="aws-resource-pinpoint-admchannel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier \(`ApplicationId`\) for the Amazon Pinpoint application that the channel is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.