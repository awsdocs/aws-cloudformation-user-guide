# AWS::MediaLive::Channel RtmpOutputSettings<a name="aws-properties-medialive-channel-rtmpoutputsettings"></a>

Configures the single output in an RTMP output group\. This element belongs to OutputSettings\.

## Syntax<a name="aws-properties-medialive-channel-rtmpoutputsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-rtmpoutputsettings-syntax.json"></a>

```
{
  "[CertificateMode](#cfn-medialive-channel-rtmpoutputsettings-certificatemode)" : String,
  "[ConnectionRetryInterval](#cfn-medialive-channel-rtmpoutputsettings-connectionretryinterval)" : Integer,
  "[Destination](#cfn-medialive-channel-rtmpoutputsettings-destination)" : OutputLocationRef,
  "[NumRetries](#cfn-medialive-channel-rtmpoutputsettings-numretries)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-rtmpoutputsettings-syntax.yaml"></a>

```
  [CertificateMode](#cfn-medialive-channel-rtmpoutputsettings-certificatemode): String
  [ConnectionRetryInterval](#cfn-medialive-channel-rtmpoutputsettings-connectionretryinterval): Integer
  [Destination](#cfn-medialive-channel-rtmpoutputsettings-destination): 
    OutputLocationRef
  [NumRetries](#cfn-medialive-channel-rtmpoutputsettings-numretries): Integer
```

## Properties<a name="aws-properties-medialive-channel-rtmpoutputsettings-properties"></a>

`CertificateMode`  <a name="cfn-medialive-channel-rtmpoutputsettings-certificatemode"></a>
If set to verifyAuthenticity, verify the tls certificate chain to a trusted Certificate Authority \(CA\)\. This will cause rtmps outputs with self\-signed certificates to fail\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionRetryInterval`  <a name="cfn-medialive-channel-rtmpoutputsettings-connectionretryinterval"></a>
Number of seconds to wait before retrying a connection to the Flash Media server if the connection is lost\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Destination`  <a name="cfn-medialive-channel-rtmpoutputsettings-destination"></a>
The RTMP endpoint excluding the stream name \(eg\. rtmp://host/appname\)\. For connection to Akamai, a username and password must be supplied\. URI fields accept format identifiers\.  
*Required*: No  
*Type*: [OutputLocationRef](aws-properties-medialive-channel-outputlocationref.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumRetries`  <a name="cfn-medialive-channel-rtmpoutputsettings-numretries"></a>
Number of retry attempts\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)