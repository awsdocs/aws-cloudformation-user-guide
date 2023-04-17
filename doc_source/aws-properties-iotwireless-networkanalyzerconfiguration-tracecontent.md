# AWS::IoTWireless::NetworkAnalyzerConfiguration TraceContent<a name="aws-properties-iotwireless-networkanalyzerconfiguration-tracecontent"></a>

Trace content for your wireless gateway and wireless device resources\.

## Syntax<a name="aws-properties-iotwireless-networkanalyzerconfiguration-tracecontent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-networkanalyzerconfiguration-tracecontent-syntax.json"></a>

```
{
  "[LogLevel](#cfn-iotwireless-networkanalyzerconfiguration-tracecontent-loglevel)" : String,
  "[WirelessDeviceFrameInfo](#cfn-iotwireless-networkanalyzerconfiguration-tracecontent-wirelessdeviceframeinfo)" : String
}
```

### YAML<a name="aws-properties-iotwireless-networkanalyzerconfiguration-tracecontent-syntax.yaml"></a>

```
  [LogLevel](#cfn-iotwireless-networkanalyzerconfiguration-tracecontent-loglevel): String
  [WirelessDeviceFrameInfo](#cfn-iotwireless-networkanalyzerconfiguration-tracecontent-wirelessdeviceframeinfo): String
```

## Properties<a name="aws-properties-iotwireless-networkanalyzerconfiguration-tracecontent-properties"></a>

`LogLevel`  <a name="cfn-iotwireless-networkanalyzerconfiguration-tracecontent-loglevel"></a>
The log level for a log message\. The log levels can be disabled, or set to `ERROR` to display less verbose logs containing only error information, or to `INFO` for more detailed logs  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WirelessDeviceFrameInfo`  <a name="cfn-iotwireless-networkanalyzerconfiguration-tracecontent-wirelessdeviceframeinfo"></a>
`FrameInfo` of your wireless device resources for the trace content\. Use FrameInfo to debug the communication between your LoRaWAN end devices and the network server\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)