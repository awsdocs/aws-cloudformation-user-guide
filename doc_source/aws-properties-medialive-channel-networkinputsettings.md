# AWS::MediaLive::Channel NetworkInputSettings<a name="aws-properties-medialive-channel-networkinputsettings"></a>

This element configures the connection to the upstream system\. This element belongs to InputSettings\.

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
You must include this element if you include a NetworkInputSettings element\.  
*Required*: No  
*Type*: [HlsInputSettings](aws-properties-medialive-channel-hlsinputsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerValidation`  <a name="cfn-medialive-channel-networkinputsettings-servervalidation"></a>
Applies only to HTTPS\. Specifies how to check HTTPS server certificates\. When set to checkCryptographyOnly, MediaLive checks the cryptography in the certificate but doesn't check the server name\. This is the recommended value for subdomains \(notably S3 buckets, which use dots in the bucket name\) that do not strictly match the corresponding certificate's wildcard pattern\. This value reduces the possibility that the validation will fail\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)