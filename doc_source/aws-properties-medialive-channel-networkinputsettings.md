# AWS::MediaLive::Channel NetworkInputSettings<a name="aws-properties-medialive-channel-networkinputsettings"></a>

Information about how to connect to the upstream system\.

The parent of this entity is InputSettings\.

## Syntax<a name="aws-properties-medialive-channel-networkinputsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-networkinputsettings-syntax.json"></a>

```
{
  "[HlsInputSettings](#cfn-medialive-channel-networkinputsettings-hlsinputsettings)" : HlsInputSettings,
  "[ServerValidation](#cfn-medialive-channel-networkinputsettings-servervalidation)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-networkinputsettings-syntax.yaml"></a>

```
  [HlsInputSettings](#cfn-medialive-channel-networkinputsettings-hlsinputsettings): 
    HlsInputSettings
  [ServerValidation](#cfn-medialive-channel-networkinputsettings-servervalidation): String
```

## Properties<a name="aws-properties-medialive-channel-networkinputsettings-properties"></a>

`HlsInputSettings`  <a name="cfn-medialive-channel-networkinputsettings-hlsinputsettings"></a>
Information about how to connect to the upstream system\.  
*Required*: No  
*Type*: [HlsInputSettings](aws-properties-medialive-channel-hlsinputsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerValidation`  <a name="cfn-medialive-channel-networkinputsettings-servervalidation"></a>
Checks HTTPS server certificates\. When set to checkCryptographyOnly, cryptography in the certificate is checked, but not the server's name\. Certain subdomains \(notably S3 buckets that use dots in the bucket name\) don't strictly match the corresponding certificate's wildcard pattern and would otherwise cause the channel to error\. This setting is ignored for protocols that do not use HTTPS\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)