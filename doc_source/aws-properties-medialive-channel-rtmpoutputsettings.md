# AWS::MediaLive::Channel RtmpOutputSettings<a name="aws-properties-medialive-channel-rtmpoutputsettings"></a>

The settings for one RTMP output\.

The parent of this entity is OutputSettings\.

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
If set to verifyAuthenticity, verifies the TLS certificate chain to a trusted certificate authority \(CA\)\. This causes RTMPS outputs with self\-signed certificates to fail\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionRetryInterval`  <a name="cfn-medialive-channel-rtmpoutputsettings-connectionretryinterval"></a>
The number of seconds to wait before retrying a connection to the Flash Media server if the connection is lost\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Destination`  <a name="cfn-medialive-channel-rtmpoutputsettings-destination"></a>
The RTMP endpoint excluding the stream name \(for example, rtmp://host/appname\)\.  
*Required*: No  
*Type*: [OutputLocationRef](aws-properties-medialive-channel-outputlocationref.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumRetries`  <a name="cfn-medialive-channel-rtmpoutputsettings-numretries"></a>
The number of retry attempts\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)