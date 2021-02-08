# AWS::IoTWireless::WirelessDevice LoRaWANDevice<a name="aws-properties-iotwireless-wirelessdevice-lorawandevice"></a>

LoRaWAN object for create functions\.

## Syntax<a name="aws-properties-iotwireless-wirelessdevice-lorawandevice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-wirelessdevice-lorawandevice-syntax.json"></a>

```
{
  "[AbpV10X](#cfn-iotwireless-wirelessdevice-lorawandevice-abpv10x)" : AbpV10X,
  "[AbpV11](#cfn-iotwireless-wirelessdevice-lorawandevice-abpv11)" : AbpV11,
  "[DevEui](#cfn-iotwireless-wirelessdevice-lorawandevice-deveui)" : String,
  "[DeviceProfileId](#cfn-iotwireless-wirelessdevice-lorawandevice-deviceprofileid)" : String,
  "[OtaaV10X](#cfn-iotwireless-wirelessdevice-lorawandevice-otaav10x)" : OtaaV10X,
  "[OtaaV11](#cfn-iotwireless-wirelessdevice-lorawandevice-otaav11)" : OtaaV11,
  "[ServiceProfileId](#cfn-iotwireless-wirelessdevice-lorawandevice-serviceprofileid)" : String
}
```

### YAML<a name="aws-properties-iotwireless-wirelessdevice-lorawandevice-syntax.yaml"></a>

```
  [AbpV10X](#cfn-iotwireless-wirelessdevice-lorawandevice-abpv10x): 
    AbpV10X
  [AbpV11](#cfn-iotwireless-wirelessdevice-lorawandevice-abpv11): 
    AbpV11
  [DevEui](#cfn-iotwireless-wirelessdevice-lorawandevice-deveui): String
  [DeviceProfileId](#cfn-iotwireless-wirelessdevice-lorawandevice-deviceprofileid): String
  [OtaaV10X](#cfn-iotwireless-wirelessdevice-lorawandevice-otaav10x): 
    OtaaV10X
  [OtaaV11](#cfn-iotwireless-wirelessdevice-lorawandevice-otaav11): 
    OtaaV11
  [ServiceProfileId](#cfn-iotwireless-wirelessdevice-lorawandevice-serviceprofileid): String
```

## Properties<a name="aws-properties-iotwireless-wirelessdevice-lorawandevice-properties"></a>

`AbpV10X`  <a name="cfn-iotwireless-wirelessdevice-lorawandevice-abpv10x"></a>
LoRaWAN object for create APIs  
*Required*: No  
*Type*: [AbpV10X](aws-properties-iotwireless-wirelessdevice-abpv10x.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AbpV11`  <a name="cfn-iotwireless-wirelessdevice-lorawandevice-abpv11"></a>
ABP device object for create APIs for v1\.1  
*Required*: No  
*Type*: [AbpV11](aws-properties-iotwireless-wirelessdevice-abpv11.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DevEui`  <a name="cfn-iotwireless-wirelessdevice-lorawandevice-deveui"></a>
The DevEUI value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceProfileId`  <a name="cfn-iotwireless-wirelessdevice-lorawandevice-deviceprofileid"></a>
The ID of the device profile for the new wireless device\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OtaaV10X`  <a name="cfn-iotwireless-wirelessdevice-lorawandevice-otaav10x"></a>
OTAA device object for create APIs for v1\.0\.x  
*Required*: No  
*Type*: [OtaaV10X](aws-properties-iotwireless-wirelessdevice-otaav10x.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OtaaV11`  <a name="cfn-iotwireless-wirelessdevice-lorawandevice-otaav11"></a>
OTAA device object for v1\.1 for create APIs  
*Required*: No  
*Type*: [OtaaV11](aws-properties-iotwireless-wirelessdevice-otaav11.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceProfileId`  <a name="cfn-iotwireless-wirelessdevice-lorawandevice-serviceprofileid"></a>
The ID of the service profile\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)