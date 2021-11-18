# AWS::IoTWireless::MulticastGroup<a name="aws-resource-iotwireless-multicastgroup"></a>

A multicast group\.

## Syntax<a name="aws-resource-iotwireless-multicastgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotwireless-multicastgroup-syntax.json"></a>

```
{
  "Type" : "AWS::IoTWireless::MulticastGroup",
  "Properties" : {
      "[AssociateWirelessDevice](#cfn-iotwireless-multicastgroup-associatewirelessdevice)" : String,
      "[Description](#cfn-iotwireless-multicastgroup-description)" : String,
      "[DisassociateWirelessDevice](#cfn-iotwireless-multicastgroup-disassociatewirelessdevice)" : String,
      "[LoRaWAN](#cfn-iotwireless-multicastgroup-lorawan)" : LoRaWAN,
      "[Name](#cfn-iotwireless-multicastgroup-name)" : String,
      "[Tags](#cfn-iotwireless-multicastgroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotwireless-multicastgroup-syntax.yaml"></a>

```
Type: AWS::IoTWireless::MulticastGroup
Properties: 
  [AssociateWirelessDevice](#cfn-iotwireless-multicastgroup-associatewirelessdevice): String
  [Description](#cfn-iotwireless-multicastgroup-description): String
  [DisassociateWirelessDevice](#cfn-iotwireless-multicastgroup-disassociatewirelessdevice): String
  [LoRaWAN](#cfn-iotwireless-multicastgroup-lorawan): 
    LoRaWAN
  [Name](#cfn-iotwireless-multicastgroup-name): String
  [Tags](#cfn-iotwireless-multicastgroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotwireless-multicastgroup-properties"></a>

`AssociateWirelessDevice`  <a name="cfn-iotwireless-multicastgroup-associatewirelessdevice"></a>
The ID of the wireless device to associate with a multicast group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-iotwireless-multicastgroup-description"></a>
The description of the multicast group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisassociateWirelessDevice`  <a name="cfn-iotwireless-multicastgroup-disassociatewirelessdevice"></a>
The ID of the wireless device to disassociate from a multicast group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoRaWAN`  <a name="cfn-iotwireless-multicastgroup-lorawan"></a>
The LoRaWAN information that is to be used with the multicast group\.  
*Required*: Yes  
*Type*: [LoRaWAN](aws-properties-iotwireless-multicastgroup-lorawan.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotwireless-multicastgroup-name"></a>
The name of the multicast group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotwireless-multicastgroup-tags"></a>
The tags are an array of key\-value pairs to attach to the specified resource\. Tags can have a minimum of 0 and a maximum of 50 items\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotwireless-multicastgroup-return-values"></a>

### Ref<a name="aws-resource-iotwireless-multicastgroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the multicast group\.

### Fn::GetAtt<a name="aws-resource-iotwireless-multicastgroup-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotwireless-multicastgroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the multicast group\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the multicast group\.

`LoRaWAN.NumberOfDevicesInGroup`  <a name="LoRaWAN.NumberOfDevicesInGroup-fn::getatt"></a>
The number of devices that are associated to the multicast group\.

`LoRaWAN.NumberOfDevicesRequested`  <a name="LoRaWAN.NumberOfDevicesRequested-fn::getatt"></a>
The number of devices that are requested to be associated with the multicast group\.

`Status`  <a name="Status-fn::getatt"></a>
The status of a multicast group\.