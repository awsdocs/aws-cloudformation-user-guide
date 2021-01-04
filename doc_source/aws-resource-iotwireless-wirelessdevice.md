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
      "[LoRaWANDevice](#cfn-iotwireless-wirelessdevice-lorawandevice)" : LoRaWANDevice,
      "[Name](#cfn-iotwireless-wirelessdevice-name)" : String,
      "[NextToken](#cfn-iotwireless-wirelessdevice-nexttoken)" : String,
      "[Tags](#cfn-iotwireless-wirelessdevice-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
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
  [LoRaWANDevice](#cfn-iotwireless-wirelessdevice-lorawandevice): 
    LoRaWANDevice
  [Name](#cfn-iotwireless-wirelessdevice-name): String
  [NextToken](#cfn-iotwireless-wirelessdevice-nexttoken): String
  [Tags](#cfn-iotwireless-wirelessdevice-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-iotwireless-wirelessdevice-type): String
```

## Properties<a name="aws-resource-iotwireless-wirelessdevice-properties"></a>

`Description`  <a name="cfn-iotwireless-wirelessdevice-description"></a>
The description of the new resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationName`  <a name="cfn-iotwireless-wirelessdevice-destinationname"></a>
The name of the destination to assign to the new wireless device\. Can have only have alphanumeric, \- \(hyphen\) and \_ \(underscore\) characters and it can't have any spaces\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoRaWANDevice`  <a name="cfn-iotwireless-wirelessdevice-lorawandevice"></a>
The device configuration information to use to create the wireless device\. Must be at least one of OtaaV10X, OtaaV11, AbpV11, or AbpV10X\.  
*Required*: No  
*Type*: [LoRaWANDevice](aws-properties-iotwireless-wirelessdevice-lorawandevice.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotwireless-wirelessdevice-name"></a>
The name of the new resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NextToken`  <a name="cfn-iotwireless-wirelessdevice-nexttoken"></a>
This parameter isn't needed to create this resource\. Do not include it in your template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotwireless-wirelessdevice-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-iotwireless-wirelessdevice-type"></a>
The wireless device type\. Must be `Sidewalk` or `LoRaWAN`\.  
*Required*: Yes  
*Type*: String  
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

`ThingArn`  <a name="ThingArn-fn::getatt"></a>
The ARN of the thing associated with the device\. The parameter is empty if a thing was not associated with the device\.

`ThingName`  <a name="ThingName-fn::getatt"></a>
The name of the thing associated with the wireless device\. The value is empty if a thing isn't associated with the device\.