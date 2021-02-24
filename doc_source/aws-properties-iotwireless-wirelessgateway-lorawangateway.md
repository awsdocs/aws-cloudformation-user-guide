# AWS::IoTWireless::WirelessGateway LoRaWANGateway<a name="aws-properties-iotwireless-wirelessgateway-lorawangateway"></a>

LoRaWAN wireless gateway object\.

## Syntax<a name="aws-properties-iotwireless-wirelessgateway-lorawangateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-wirelessgateway-lorawangateway-syntax.json"></a>

```
{
  "[GatewayEui](#cfn-iotwireless-wirelessgateway-lorawangateway-gatewayeui)" : String,
  "[RfRegion](#cfn-iotwireless-wirelessgateway-lorawangateway-rfregion)" : String
}
```

### YAML<a name="aws-properties-iotwireless-wirelessgateway-lorawangateway-syntax.yaml"></a>

```
  [GatewayEui](#cfn-iotwireless-wirelessgateway-lorawangateway-gatewayeui): String
  [RfRegion](#cfn-iotwireless-wirelessgateway-lorawangateway-rfregion): String
```

## Properties<a name="aws-properties-iotwireless-wirelessgateway-lorawangateway-properties"></a>

`GatewayEui`  <a name="cfn-iotwireless-wirelessgateway-lorawangateway-gatewayeui"></a>
The gateway's EUI value, with the pattern `^(([0-9A-Fa-f]{2}-){7}|([0-9A-Fa-f]{2}:){7}|([0-9A-Fa-f]{2}\s){7}|([0-9A-Fa-f]{2}){7})([0-9A-Fa-f]{2})$`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RfRegion`  <a name="cfn-iotwireless-wirelessgateway-lorawangateway-rfregion"></a>
The frequency band \(RFRegion\) value\. Maximum length is 64\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)