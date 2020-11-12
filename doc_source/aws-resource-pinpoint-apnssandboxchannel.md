# AWS::Pinpoint::APNSSandboxChannel<a name="aws-resource-pinpoint-apnssandboxchannel"></a>

A *channel* is a type of platform that you can deliver messages to\. You can use the APNs sandbox channel to send push notification messages to the sandbox environment of the Apple Push Notification service \(APNs\)\. Before you can use Amazon Pinpoint to send notifications to the APNs sandbox environment, you have to enable the APNs sandbox channel for an Amazon Pinpoint application\.

The AWS::Pinpoint::APNSSandboxChannel resource defines the status and authentication settings of the APNs sandbox channel for an application\.

## Syntax<a name="aws-resource-pinpoint-apnssandboxchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-apnssandboxchannel-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::APNSSandboxChannel",
  "Properties" : {
      "[ApplicationId](#cfn-pinpoint-apnssandboxchannel-applicationid)" : String,
      "[BundleId](#cfn-pinpoint-apnssandboxchannel-bundleid)" : String,
      "[Certificate](#cfn-pinpoint-apnssandboxchannel-certificate)" : String,
      "[DefaultAuthenticationMethod](#cfn-pinpoint-apnssandboxchannel-defaultauthenticationmethod)" : String,
      "[Enabled](#cfn-pinpoint-apnssandboxchannel-enabled)" : Boolean,
      "[PrivateKey](#cfn-pinpoint-apnssandboxchannel-privatekey)" : String,
      "[TeamId](#cfn-pinpoint-apnssandboxchannel-teamid)" : String,
      "[TokenKey](#cfn-pinpoint-apnssandboxchannel-tokenkey)" : String,
      "[TokenKeyId](#cfn-pinpoint-apnssandboxchannel-tokenkeyid)" : String
    }
}
```

### YAML<a name="aws-resource-pinpoint-apnssandboxchannel-syntax.yaml"></a>

```
Type: AWS::Pinpoint::APNSSandboxChannel
Properties: 
  [ApplicationId](#cfn-pinpoint-apnssandboxchannel-applicationid): String
  [BundleId](#cfn-pinpoint-apnssandboxchannel-bundleid): String
  [Certificate](#cfn-pinpoint-apnssandboxchannel-certificate): String
  [DefaultAuthenticationMethod](#cfn-pinpoint-apnssandboxchannel-defaultauthenticationmethod): String
  [Enabled](#cfn-pinpoint-apnssandboxchannel-enabled): Boolean
  [PrivateKey](#cfn-pinpoint-apnssandboxchannel-privatekey): String
  [TeamId](#cfn-pinpoint-apnssandboxchannel-teamid): String
  [TokenKey](#cfn-pinpoint-apnssandboxchannel-tokenkey): String
  [TokenKeyId](#cfn-pinpoint-apnssandboxchannel-tokenkeyid): String
```

## Properties<a name="aws-resource-pinpoint-apnssandboxchannel-properties"></a>

`ApplicationId`  <a name="cfn-pinpoint-apnssandboxchannel-applicationid"></a>
The unique identifier for the application that the APNs sandbox channel applies to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BundleId`  <a name="cfn-pinpoint-apnssandboxchannel-bundleid"></a>
The bundle identifier that's assigned to your iOS app\. This identifier is used for APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Certificate`  <a name="cfn-pinpoint-apnssandboxchannel-certificate"></a>
The APNs client certificate that you received from Apple, if you want Amazon Pinpoint to communicate with the APNs sandbox environment by using an APNs certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultAuthenticationMethod`  <a name="cfn-pinpoint-apnssandboxchannel-defaultauthenticationmethod"></a>
The default authentication method that you want Amazon Pinpoint to use when authenticating with the APNs sandbox environment, key or certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-pinpoint-apnssandboxchannel-enabled"></a>
Specifies whether to enable the APNs sandbox channel for the application\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKey`  <a name="cfn-pinpoint-apnssandboxchannel-privatekey"></a>
The private key for the APNs client certificate that you want Amazon Pinpoint to use to communicate with the APNs sandbox environment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TeamId`  <a name="cfn-pinpoint-apnssandboxchannel-teamid"></a>
The identifier that's assigned to your Apple developer account team\. This identifier is used for APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenKey`  <a name="cfn-pinpoint-apnssandboxchannel-tokenkey"></a>
The authentication key to use for APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenKeyId`  <a name="cfn-pinpoint-apnssandboxchannel-tokenkeyid"></a>
The key identifier that's assigned to your APNs signing key, if you want Amazon Pinpoint to communicate with the APNs sandbox environment by using APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpoint-apnssandboxchannel-return-values"></a>

### Ref<a name="aws-resource-pinpoint-apnssandboxchannel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier \(`ApplicationId`\) for the Amazon Pinpoint application that the channel is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.