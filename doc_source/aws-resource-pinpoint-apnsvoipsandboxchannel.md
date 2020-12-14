# AWS::Pinpoint::APNSVoipSandboxChannel<a name="aws-resource-pinpoint-apnsvoipsandboxchannel"></a>

A *channel* is a type of platform that you can deliver messages to\. You can use the APNs VoIP sandbox channel to send VoIP notification messages to the sandbox environment of the Apple Push Notification service \(APNs\)\. Before you can use Amazon Pinpoint to send VoIP notifications to the APNs sandbox environment, you have to enable the APNs VoIP sandbox channel for an Amazon Pinpoint application\.

The AWS::Pinpoint::APNSVoipSandboxChannel resource defines the status and authentication settings of the APNs VoIP sandbox channel for an application\.

## Syntax<a name="aws-resource-pinpoint-apnsvoipsandboxchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-apnsvoipsandboxchannel-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::APNSVoipSandboxChannel",
  "Properties" : {
      "[ApplicationId](#cfn-pinpoint-apnsvoipsandboxchannel-applicationid)" : String,
      "[BundleId](#cfn-pinpoint-apnsvoipsandboxchannel-bundleid)" : String,
      "[Certificate](#cfn-pinpoint-apnsvoipsandboxchannel-certificate)" : String,
      "[DefaultAuthenticationMethod](#cfn-pinpoint-apnsvoipsandboxchannel-defaultauthenticationmethod)" : String,
      "[Enabled](#cfn-pinpoint-apnsvoipsandboxchannel-enabled)" : Boolean,
      "[PrivateKey](#cfn-pinpoint-apnsvoipsandboxchannel-privatekey)" : String,
      "[TeamId](#cfn-pinpoint-apnsvoipsandboxchannel-teamid)" : String,
      "[TokenKey](#cfn-pinpoint-apnsvoipsandboxchannel-tokenkey)" : String,
      "[TokenKeyId](#cfn-pinpoint-apnsvoipsandboxchannel-tokenkeyid)" : String
    }
}
```

### YAML<a name="aws-resource-pinpoint-apnsvoipsandboxchannel-syntax.yaml"></a>

```
Type: AWS::Pinpoint::APNSVoipSandboxChannel
Properties: 
  [ApplicationId](#cfn-pinpoint-apnsvoipsandboxchannel-applicationid): String
  [BundleId](#cfn-pinpoint-apnsvoipsandboxchannel-bundleid): String
  [Certificate](#cfn-pinpoint-apnsvoipsandboxchannel-certificate): String
  [DefaultAuthenticationMethod](#cfn-pinpoint-apnsvoipsandboxchannel-defaultauthenticationmethod): String
  [Enabled](#cfn-pinpoint-apnsvoipsandboxchannel-enabled): Boolean
  [PrivateKey](#cfn-pinpoint-apnsvoipsandboxchannel-privatekey): String
  [TeamId](#cfn-pinpoint-apnsvoipsandboxchannel-teamid): String
  [TokenKey](#cfn-pinpoint-apnsvoipsandboxchannel-tokenkey): String
  [TokenKeyId](#cfn-pinpoint-apnsvoipsandboxchannel-tokenkeyid): String
```

## Properties<a name="aws-resource-pinpoint-apnsvoipsandboxchannel-properties"></a>

`ApplicationId`  <a name="cfn-pinpoint-apnsvoipsandboxchannel-applicationid"></a>
The unique identifier for the application that the APNs VoIP sandbox channel applies to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BundleId`  <a name="cfn-pinpoint-apnsvoipsandboxchannel-bundleid"></a>
The bundle identifier that's assigned to your iOS app\. This identifier is used for APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Certificate`  <a name="cfn-pinpoint-apnsvoipsandboxchannel-certificate"></a>
The APNs client certificate that you received from Apple, if you want Amazon Pinpoint to communicate with the APNs sandbox environment by using an APNs certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultAuthenticationMethod`  <a name="cfn-pinpoint-apnsvoipsandboxchannel-defaultauthenticationmethod"></a>
The default authentication method that you want Amazon Pinpoint to use when authenticating with the APNs sandbox environment for this channel, key or certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-pinpoint-apnsvoipsandboxchannel-enabled"></a>
Specifies whether the APNs VoIP sandbox channel is enabled for the application\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKey`  <a name="cfn-pinpoint-apnsvoipsandboxchannel-privatekey"></a>
The private key for the APNs client certificate that you want Amazon Pinpoint to use to communicate with the APNs sandbox environment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TeamId`  <a name="cfn-pinpoint-apnsvoipsandboxchannel-teamid"></a>
The identifier that's assigned to your Apple developer account team\. This identifier is used for APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenKey`  <a name="cfn-pinpoint-apnsvoipsandboxchannel-tokenkey"></a>
The authentication key to use for APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenKeyId`  <a name="cfn-pinpoint-apnsvoipsandboxchannel-tokenkeyid"></a>
The key identifier that's assigned to your APNs signing key, if you want Amazon Pinpoint to communicate with the APNs sandbox environment by using APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpoint-apnsvoipsandboxchannel-return-values"></a>

### Ref<a name="aws-resource-pinpoint-apnsvoipsandboxchannel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier \(`ApplicationId`\) for the Amazon Pinpoint application that the channel is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.