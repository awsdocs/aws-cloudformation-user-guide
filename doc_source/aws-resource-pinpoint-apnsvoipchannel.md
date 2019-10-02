# AWS::Pinpoint::APNSVoipChannel<a name="aws-resource-pinpoint-apnsvoipchannel"></a>

A *channel* is a type of platform that you can deliver messages to\. You can use the APNs VoIP channel to send VoIP notification messages to the Apple Push Notification service \(APNs\)\. Before you use Amazon Pinpoint to send VoIP notifications to APNs, you have to enable the APNs VoIP channel for an Amazon Pinpoint app\.

The APNs VoIP Channel resource represents the status and authentication settings of the APNs VoIP channel for a specific application\. You can use this resource to retrieve information about, update, or disable \(delete\) the APNs VoIP channel for an application\.

## Syntax<a name="aws-resource-pinpoint-apnsvoipchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-apnsvoipchannel-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::APNSVoipChannel",
  "Properties" : {
      "[ApplicationId](#cfn-pinpoint-apnsvoipchannel-applicationid)" : String,
      "[BundleId](#cfn-pinpoint-apnsvoipchannel-bundleid)" : String,
      "[Certificate](#cfn-pinpoint-apnsvoipchannel-certificate)" : String,
      "[DefaultAuthenticationMethod](#cfn-pinpoint-apnsvoipchannel-defaultauthenticationmethod)" : String,
      "[Enabled](#cfn-pinpoint-apnsvoipchannel-enabled)" : Boolean,
      "[PrivateKey](#cfn-pinpoint-apnsvoipchannel-privatekey)" : String,
      "[TeamId](#cfn-pinpoint-apnsvoipchannel-teamid)" : String,
      "[TokenKey](#cfn-pinpoint-apnsvoipchannel-tokenkey)" : String,
      "[TokenKeyId](#cfn-pinpoint-apnsvoipchannel-tokenkeyid)" : String
    }
}
```

### YAML<a name="aws-resource-pinpoint-apnsvoipchannel-syntax.yaml"></a>

```
Type: AWS::Pinpoint::APNSVoipChannel
Properties: 
  [ApplicationId](#cfn-pinpoint-apnsvoipchannel-applicationid): String
  [BundleId](#cfn-pinpoint-apnsvoipchannel-bundleid): String
  [Certificate](#cfn-pinpoint-apnsvoipchannel-certificate): String
  [DefaultAuthenticationMethod](#cfn-pinpoint-apnsvoipchannel-defaultauthenticationmethod): String
  [Enabled](#cfn-pinpoint-apnsvoipchannel-enabled): Boolean
  [PrivateKey](#cfn-pinpoint-apnsvoipchannel-privatekey): String
  [TeamId](#cfn-pinpoint-apnsvoipchannel-teamid): String
  [TokenKey](#cfn-pinpoint-apnsvoipchannel-tokenkey): String
  [TokenKeyId](#cfn-pinpoint-apnsvoipchannel-tokenkeyid): String
```

## Properties<a name="aws-resource-pinpoint-apnsvoipchannel-properties"></a>

`ApplicationId`  <a name="cfn-pinpoint-apnsvoipchannel-applicationid"></a>
The unique identifier of the Amazon Pinpoint application that the APNs VoIP channel applies to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BundleId`  <a name="cfn-pinpoint-apnsvoipchannel-bundleid"></a>
The bundle identifier that's assigned to your iOS app\. This identifier is used for APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Certificate`  <a name="cfn-pinpoint-apnsvoipchannel-certificate"></a>
The APNs client certificate that you received from Apple\. Specify this value if you want Amazon Pinpoint to communicate with APNs by using an APNs certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultAuthenticationMethod`  <a name="cfn-pinpoint-apnsvoipchannel-defaultauthenticationmethod"></a>
The default authentication method that you want Amazon Pinpoint to use when authenticating with APNs\. Valid options are `key` or `certificate`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-pinpoint-apnsvoipchannel-enabled"></a>
Specifies whether to enable the APNs VoIP channel for the Amazon Pinpoint application\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKey`  <a name="cfn-pinpoint-apnsvoipchannel-privatekey"></a>
The private key for the APNs client certificate that you want Amazon Pinpoint to use to communicate with APNs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TeamId`  <a name="cfn-pinpoint-apnsvoipchannel-teamid"></a>
The identifier that's assigned to your Apple Developer Account team\. This identifier is used for APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenKey`  <a name="cfn-pinpoint-apnsvoipchannel-tokenkey"></a>
The authentication key to use for APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenKeyId`  <a name="cfn-pinpoint-apnsvoipchannel-tokenkeyid"></a>
The key identifier that's assigned to your APNs signing key\. Specify this value if you want Amazon Pinpoint to communicate with APNs by using APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-pinpoint-apnsvoipchannel-return-values"></a>

### Ref<a name="aws-resource-pinpoint-apnsvoipchannel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Amazon Pinpoint app that the channel is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-south-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-west-2`
