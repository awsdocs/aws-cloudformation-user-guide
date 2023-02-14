# AWS::IoTWireless::WirelessDevice<a name="aws-resource-iotwireless-wirelessdevice"></a>

Provisions a wireless device\.

## Syntax<a name="aws-resource-iotwireless-wirelessdevice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotwireless-wirelessdevice-syntax.json"></a>

```
{
  "Type" : "AWS::IoTWireless::WirelessDevice",
  "Properties" : {
      "[Description](#cfn-iotwireless-wirelessdevice-description)" : String,
      "[DestinationName](#cfn-iotwireless-wirelessdevice-destinationname)" : String,
      "[LastUplinkReceivedAt](#cfn-iotwireless-wirelessdevice-lastuplinkreceivedat)" : String,
      "[LoRaWAN](#cfn-iotwireless-wirelessdevice-lorawan)" : LoRaWANDevice,
      "[Name](#cfn-iotwireless-wirelessdevice-name)" : String,
      "[Tags](#cfn-iotwireless-wirelessdevice-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[ThingArn](#cfn-iotwireless-wirelessdevice-thingarn)" : String,
      "[Type](#cfn-iotwireless-wirelessdevice-type)" : String
    }
}
```

### YAML<a name="aws-resource-iotwireless-wirelessdevice-syntax.yaml"></a>

```
Type: AWS::IoTWireless::WirelessDevice
Properties: 
  [Description](#cfn-iotwireless-wirelessdevice-description): String
  [DestinationName](#cfn-iotwireless-wirelessdevice-destinationname): String
  [LastUplinkReceivedAt](#cfn-iotwireless-wirelessdevice-lastuplinkreceivedat): String
  [LoRaWAN](#cfn-iotwireless-wirelessdevice-lorawan): 
    LoRaWANDevice
  [Name](#cfn-iotwireless-wirelessdevice-name): String
  [Tags](#cfn-iotwireless-wirelessdevice-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [ThingArn](#cfn-iotwireless-wirelessdevice-thingarn): String
  [Type](#cfn-iotwireless-wirelessdevice-type): String
```

## Properties<a name="aws-resource-iotwireless-wirelessdevice-properties"></a>

`Description`  <a name="cfn-iotwireless-wirelessdevice-description"></a>
The description of the new resource\. Maximum length is 2048\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationName`  <a name="cfn-iotwireless-wirelessdevice-destinationname"></a>
The name of the destination to assign to the new wireless device\. Can have only have alphanumeric, \- \(hyphen\) and \_ \(underscore\) characters and it can't have any spaces\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9-_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LastUplinkReceivedAt`  <a name="cfn-iotwireless-wirelessdevice-lastuplinkreceivedat"></a>
The date and time when the most recent uplink was received\.  
*Required*: No  
*Type*: String  
*Pattern*: `^([\+-]?\d{4}(?!\d{2}\b))((-?)((0[1-9]|1[0-2])(\3([12]\d|0[1-9]|3[01]))?|W([0-4]\d|5[0-2])(-?[1-7])?|(00[1-9]|0[1-9]\d|[12]\d{2}|3([0-5]\d|6[1-6])))([T\s]((([01]\d|2[0-3])((:?)[0-5]\d)?|24\:?00)([\.,]\d+(?!:))?)?(\17[0-5]\d([\.,]\d+)?)?([zZ]|([\+-])([01]\d|2[0-3]):?([0-5]\d)?)?)?)?$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoRaWAN`  <a name="cfn-iotwireless-wirelessdevice-lorawan"></a>
The device configuration information to use to create the wireless device\. Must be at least one of OtaaV10x, OtaaV11, AbpV11, or AbpV10x\.  
*Required*: No  
*Type*: [LoRaWANDevice](aws-properties-iotwireless-wirelessdevice-lorawandevice.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotwireless-wirelessdevice-name"></a>
The name of the new resource\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotwireless-wirelessdevice-tags"></a>
The tags are an array of key\-value pairs to attach to the specified resource\. Tags can have a minimum of 0 and a maximum of 50 items\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThingArn`  <a name="cfn-iotwireless-wirelessdevice-thingarn"></a>
The ARN of the thing to associate with the wireless device\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-iotwireless-wirelessdevice-type"></a>
The wireless device type\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `LoRaWAN | Sidewalk`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotwireless-wirelessdevice-return-values"></a>

### Ref<a name="aws-resource-iotwireless-wirelessdevice-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the wireless device ID\.

### Fn::GetAtt<a name="aws-resource-iotwireless-wirelessdevice-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotwireless-wirelessdevice-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the wireless device created\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the wireless device created\.

`ThingName`  <a name="ThingName-fn::getatt"></a>
The name of the thing associated with the wireless device\. The value is empty if a thing isn't associated with the device\.