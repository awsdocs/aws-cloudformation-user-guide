# AWS::IoTWireless::FuotaTask LoRaWAN<a name="aws-properties-iotwireless-fuotatask-lorawan"></a>

The LoRaWAN information used with a FUOTA task\.

## Syntax<a name="aws-properties-iotwireless-fuotatask-lorawan-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-fuotatask-lorawan-syntax.json"></a>

```
{
  "[RfRegion](#cfn-iotwireless-fuotatask-lorawan-rfregion)" : String,
  "[StartTime](#cfn-iotwireless-fuotatask-lorawan-starttime)" : String
}
```

### YAML<a name="aws-properties-iotwireless-fuotatask-lorawan-syntax.yaml"></a>

```
  [RfRegion](#cfn-iotwireless-fuotatask-lorawan-rfregion): String
  [StartTime](#cfn-iotwireless-fuotatask-lorawan-starttime): String
```

## Properties<a name="aws-properties-iotwireless-fuotatask-lorawan-properties"></a>

`RfRegion`  <a name="cfn-iotwireless-fuotatask-lorawan-rfregion"></a>
The frequency band \(RFRegion\) value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartTime`  <a name="cfn-iotwireless-fuotatask-lorawan-starttime"></a>
Start time of a FUOTA task\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)