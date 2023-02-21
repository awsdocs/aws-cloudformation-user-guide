# AWS::IoTFleetWise::DecoderManifest ObdSignal<a name="aws-properties-iotfleetwise-decodermanifest-obdsignal"></a>

Information about signal messages using the on\-board diagnostics \(OBD\) II protocol in a vehicle\.

## Syntax<a name="aws-properties-iotfleetwise-decodermanifest-obdsignal-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-decodermanifest-obdsignal-syntax.json"></a>

```
{
  "[BitMaskLength](#cfn-iotfleetwise-decodermanifest-obdsignal-bitmasklength)" : String,
  "[BitRightShift](#cfn-iotfleetwise-decodermanifest-obdsignal-bitrightshift)" : String,
  "[ByteLength](#cfn-iotfleetwise-decodermanifest-obdsignal-bytelength)" : String,
  "[Offset](#cfn-iotfleetwise-decodermanifest-obdsignal-offset)" : String,
  "[Pid](#cfn-iotfleetwise-decodermanifest-obdsignal-pid)" : String,
  "[PidResponseLength](#cfn-iotfleetwise-decodermanifest-obdsignal-pidresponselength)" : String,
  "[Scaling](#cfn-iotfleetwise-decodermanifest-obdsignal-scaling)" : String,
  "[ServiceMode](#cfn-iotfleetwise-decodermanifest-obdsignal-servicemode)" : String,
  "[StartByte](#cfn-iotfleetwise-decodermanifest-obdsignal-startbyte)" : String
}
```

### YAML<a name="aws-properties-iotfleetwise-decodermanifest-obdsignal-syntax.yaml"></a>

```
  [BitMaskLength](#cfn-iotfleetwise-decodermanifest-obdsignal-bitmasklength): String
  [BitRightShift](#cfn-iotfleetwise-decodermanifest-obdsignal-bitrightshift): String
  [ByteLength](#cfn-iotfleetwise-decodermanifest-obdsignal-bytelength): String
  [Offset](#cfn-iotfleetwise-decodermanifest-obdsignal-offset): String
  [Pid](#cfn-iotfleetwise-decodermanifest-obdsignal-pid): String
  [PidResponseLength](#cfn-iotfleetwise-decodermanifest-obdsignal-pidresponselength): String
  [Scaling](#cfn-iotfleetwise-decodermanifest-obdsignal-scaling): String
  [ServiceMode](#cfn-iotfleetwise-decodermanifest-obdsignal-servicemode): String
  [StartByte](#cfn-iotfleetwise-decodermanifest-obdsignal-startbyte): String
```

## Properties<a name="aws-properties-iotfleetwise-decodermanifest-obdsignal-properties"></a>

`BitMaskLength`  <a name="cfn-iotfleetwise-decodermanifest-obdsignal-bitmasklength"></a>
The number of bits to mask in a message\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `8`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BitRightShift`  <a name="cfn-iotfleetwise-decodermanifest-obdsignal-bitrightshift"></a>
The number of positions to shift bits in the message\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ByteLength`  <a name="cfn-iotfleetwise-decodermanifest-obdsignal-bytelength"></a>
The length of a message\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `8`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Offset`  <a name="cfn-iotfleetwise-decodermanifest-obdsignal-offset"></a>
Indicates where data appears in the message\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Pid`  <a name="cfn-iotfleetwise-decodermanifest-obdsignal-pid"></a>
The diagnostic code used to request data from a vehicle for this signal\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PidResponseLength`  <a name="cfn-iotfleetwise-decodermanifest-obdsignal-pidresponselength"></a>
The length of the requested data\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scaling`  <a name="cfn-iotfleetwise-decodermanifest-obdsignal-scaling"></a>
A multiplier used to decode the message\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceMode`  <a name="cfn-iotfleetwise-decodermanifest-obdsignal-servicemode"></a>
The mode of operation \(diagnostic service\) in a message\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartByte`  <a name="cfn-iotfleetwise-decodermanifest-obdsignal-startbyte"></a>
Indicates the beginning of the message\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)