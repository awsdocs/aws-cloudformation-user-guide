# AWS::IoTFleetWise::DecoderManifest SignalDecodersItems<a name="aws-properties-iotfleetwise-decodermanifest-signaldecodersitems"></a>

Information about a signal decoder\.

## Syntax<a name="aws-properties-iotfleetwise-decodermanifest-signaldecodersitems-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-decodermanifest-signaldecodersitems-syntax.json"></a>

```
{
  "[CanSignal](#cfn-iotfleetwise-decodermanifest-signaldecodersitems-cansignal)" : CanSignal,
  "[FullyQualifiedName](#cfn-iotfleetwise-decodermanifest-signaldecodersitems-fullyqualifiedname)" : String,
  "[InterfaceId](#cfn-iotfleetwise-decodermanifest-signaldecodersitems-interfaceid)" : String,
  "[ObdSignal](#cfn-iotfleetwise-decodermanifest-signaldecodersitems-obdsignal)" : ObdSignal,
  "[Type](#cfn-iotfleetwise-decodermanifest-signaldecodersitems-type)" : String
}
```

### YAML<a name="aws-properties-iotfleetwise-decodermanifest-signaldecodersitems-syntax.yaml"></a>

```
  [CanSignal](#cfn-iotfleetwise-decodermanifest-signaldecodersitems-cansignal): 
    CanSignal
  [FullyQualifiedName](#cfn-iotfleetwise-decodermanifest-signaldecodersitems-fullyqualifiedname): String
  [InterfaceId](#cfn-iotfleetwise-decodermanifest-signaldecodersitems-interfaceid): String
  [ObdSignal](#cfn-iotfleetwise-decodermanifest-signaldecodersitems-obdsignal): 
    ObdSignal
  [Type](#cfn-iotfleetwise-decodermanifest-signaldecodersitems-type): String
```

## Properties<a name="aws-properties-iotfleetwise-decodermanifest-signaldecodersitems-properties"></a>

`CanSignal`  <a name="cfn-iotfleetwise-decodermanifest-signaldecodersitems-cansignal"></a>
\(Optional\) Information about a single controller area network \(CAN\) signal and the messages it receives and transmits\.  
*Required*: No  
*Type*: [CanSignal](aws-properties-iotfleetwise-decodermanifest-cansignal.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FullyQualifiedName`  <a name="cfn-iotfleetwise-decodermanifest-signaldecodersitems-fullyqualifiedname"></a>
The fully qualified name of a signal decoder as defined in a vehicle model\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `150`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InterfaceId`  <a name="cfn-iotfleetwise-decodermanifest-signaldecodersitems-interfaceid"></a>
The ID of a network interface that specifies what network protocol a vehicle follows\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObdSignal`  <a name="cfn-iotfleetwise-decodermanifest-signaldecodersitems-obdsignal"></a>
\(Optional\) Information about signal messages using the on\-board diagnostics \(OBD\) II protocol in a vehicle\.  
*Required*: No  
*Type*: [ObdSignal](aws-properties-iotfleetwise-decodermanifest-obdsignal.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-iotfleetwise-decodermanifest-signaldecodersitems-type"></a>
The network protocol for the vehicle\. For example, `CAN_SIGNAL` specifies a protocol that defines how data is communicated between electronic control units \(ECUs\)\. `OBD_SIGNAL` specifies a protocol that defines how self\-diagnostic data is communicated between ECUs\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CAN_SIGNAL | OBD_SIGNAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)