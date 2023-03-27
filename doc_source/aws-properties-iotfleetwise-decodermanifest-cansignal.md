# AWS::IoTFleetWise::DecoderManifest CanSignal<a name="aws-properties-iotfleetwise-decodermanifest-cansignal"></a>

Information about a single controller area network \(CAN\) signal and the messages it receives and transmits\.

## Syntax<a name="aws-properties-iotfleetwise-decodermanifest-cansignal-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-decodermanifest-cansignal-syntax.json"></a>

```
{
  "[Factor](#cfn-iotfleetwise-decodermanifest-cansignal-factor)" : String,
  "[IsBigEndian](#cfn-iotfleetwise-decodermanifest-cansignal-isbigendian)" : String,
  "[IsSigned](#cfn-iotfleetwise-decodermanifest-cansignal-issigned)" : String,
  "[Length](#cfn-iotfleetwise-decodermanifest-cansignal-length)" : String,
  "[MessageId](#cfn-iotfleetwise-decodermanifest-cansignal-messageid)" : String,
  "[Name](#cfn-iotfleetwise-decodermanifest-cansignal-name)" : String,
  "[Offset](#cfn-iotfleetwise-decodermanifest-cansignal-offset)" : String,
  "[StartBit](#cfn-iotfleetwise-decodermanifest-cansignal-startbit)" : String
}
```

### YAML<a name="aws-properties-iotfleetwise-decodermanifest-cansignal-syntax.yaml"></a>

```
  [Factor](#cfn-iotfleetwise-decodermanifest-cansignal-factor): String
  [IsBigEndian](#cfn-iotfleetwise-decodermanifest-cansignal-isbigendian): String
  [IsSigned](#cfn-iotfleetwise-decodermanifest-cansignal-issigned): String
  [Length](#cfn-iotfleetwise-decodermanifest-cansignal-length): String
  [MessageId](#cfn-iotfleetwise-decodermanifest-cansignal-messageid): String
  [Name](#cfn-iotfleetwise-decodermanifest-cansignal-name): String
  [Offset](#cfn-iotfleetwise-decodermanifest-cansignal-offset): String
  [StartBit](#cfn-iotfleetwise-decodermanifest-cansignal-startbit): String
```

## Properties<a name="aws-properties-iotfleetwise-decodermanifest-cansignal-properties"></a>

`Factor`  <a name="cfn-iotfleetwise-decodermanifest-cansignal-factor"></a>
A multiplier used to decode the CAN message\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsBigEndian`  <a name="cfn-iotfleetwise-decodermanifest-cansignal-isbigendian"></a>
Whether the byte ordering of a CAN message is big\-endian\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsSigned`  <a name="cfn-iotfleetwise-decodermanifest-cansignal-issigned"></a>
Whether the message data is specified as a signed value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Length`  <a name="cfn-iotfleetwise-decodermanifest-cansignal-length"></a>
How many bytes of data are in the message\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageId`  <a name="cfn-iotfleetwise-decodermanifest-cansignal-messageid"></a>
The ID of the message\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotfleetwise-decodermanifest-cansignal-name"></a>
The name of the signal\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Offset`  <a name="cfn-iotfleetwise-decodermanifest-cansignal-offset"></a>
Indicates where data appears in the CAN message\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartBit`  <a name="cfn-iotfleetwise-decodermanifest-cansignal-startbit"></a>
Indicates the beginning of the CAN message\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)