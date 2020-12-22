# AWS::IoTWireless::WirelessDevice AbpV10X<a name="aws-properties-iotwireless-wirelessdevice-abpv10x"></a>

ABP device object for LoRaWAN specification v1\.0\.x

## Syntax<a name="aws-properties-iotwireless-wirelessdevice-abpv10x-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-wirelessdevice-abpv10x-syntax.json"></a>

```
{
  "[DevAddr](#cfn-iotwireless-wirelessdevice-abpv10x-devaddr)" : String,
  "[SessionKeys](#cfn-iotwireless-wirelessdevice-abpv10x-sessionkeys)" : SessionKeysAbpV10X
}
```

### YAML<a name="aws-properties-iotwireless-wirelessdevice-abpv10x-syntax.yaml"></a>

```
  [DevAddr](#cfn-iotwireless-wirelessdevice-abpv10x-devaddr): String
  [SessionKeys](#cfn-iotwireless-wirelessdevice-abpv10x-sessionkeys): 
    SessionKeysAbpV10X
```

## Properties<a name="aws-properties-iotwireless-wirelessdevice-abpv10x-properties"></a>

`DevAddr`  <a name="cfn-iotwireless-wirelessdevice-abpv10x-devaddr"></a>
The DevAddr value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionKeys`  <a name="cfn-iotwireless-wirelessdevice-abpv10x-sessionkeys"></a>
Session keys for ABP v1\.0\.x  
*Required*: No  
*Type*: [SessionKeysAbpV10X](aws-properties-iotwireless-wirelessdevice-sessionkeysabpv10x.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)