# AWS::Pinpoint::APNSVoipChannel<a name="aws-resource-pinpoint-apnsvoipchannel"></a>

A *channel* is a type of platform that you can deliver messages to\. You can use the APNs VoIP channel to send VoIP notification messages to the Apple Push Notification service \(APNs\)\. Before you can use Amazon Pinpoint to send VoIP notifications to APNs, you have to enable the APNs VoIP channel for an Amazon Pinpoint application\.

The AWS::Pinpoint::APNSVoipChannel resource defines the status and authentication settings of the APNs VoIP channel for an application\.

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
The unique identifier for the application that the APNs VoIP channel applies to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BundleId`  <a name="cfn-pinpoint-apnsvoipchannel-bundleid"></a>
The bundle identifier that's assigned to your iOS app\. This identifier is used for APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Certificate`  <a name="cfn-pinpoint-apnsvoipchannel-certificate"></a>
The APNs client certificate that you received from Apple, if you want Amazon Pinpoint to communicate with APNs by using an APNs certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultAuthenticationMethod`  <a name="cfn-pinpoint-apnsvoipchannel-defaultauthenticationmethod"></a>
The default authentication method that you want Amazon Pinpoint to use when authenticating with APNs, key or certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-pinpoint-apnsvoipchannel-enabled"></a>
Specifies whether to enable the APNs VoIP channel for the application\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKey`  <a name="cfn-pinpoint-apnsvoipchannel-privatekey"></a>
The private key for the APNs client certificate that you want Amazon Pinpoint to use to communicate with APNs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TeamId`  <a name="cfn-pinpoint-apnsvoipchannel-teamid"></a>
The identifier that's assigned to your Apple developer account team\. This identifier is used for APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenKey`  <a name="cfn-pinpoint-apnsvoipchannel-tokenkey"></a>
The key identifier that's assigned to your APNs signing key, if you want Amazon Pinpoint to communicate with APNs by using APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenKeyId`  <a name="cfn-pinpoint-apnsvoipchannel-tokenkeyid"></a>
The key identifier that's assigned to your APNs signing key, if you want Amazon Pinpoint to communicate with APNs by using APNs tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpoint-apnsvoipchannel-return-values"></a>

### Ref<a name="aws-resource-pinpoint-apnsvoipchannel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier \(`ApplicationId`\) for the Amazon Pinpoint application that the channel is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.