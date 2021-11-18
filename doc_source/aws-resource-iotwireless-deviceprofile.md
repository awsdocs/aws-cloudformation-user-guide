# AWS::IoTWireless::DeviceProfile<a name="aws-resource-iotwireless-deviceprofile"></a>

Creates a new device profile\.

## Syntax<a name="aws-resource-iotwireless-deviceprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotwireless-deviceprofile-syntax.json"></a>

```
{
  "Type" : "AWS::IoTWireless::DeviceProfile",
  "Properties" : {
      "[LoRaWAN](#cfn-iotwireless-deviceprofile-lorawan)" : LoRaWANDeviceProfile,
      "[Name](#cfn-iotwireless-deviceprofile-name)" : String,
      "[Tags](#cfn-iotwireless-deviceprofile-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotwireless-deviceprofile-syntax.yaml"></a>

```
Type: AWS::IoTWireless::DeviceProfile
Properties: 
  [LoRaWAN](#cfn-iotwireless-deviceprofile-lorawan): 
    LoRaWANDeviceProfile
  [Name](#cfn-iotwireless-deviceprofile-name): String
  [Tags](#cfn-iotwireless-deviceprofile-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotwireless-deviceprofile-properties"></a>

`LoRaWAN`  <a name="cfn-iotwireless-deviceprofile-lorawan"></a>
LoRaWAN device profile object\.  
*Required*: No  
*Type*: [LoRaWANDeviceProfile](aws-properties-iotwireless-deviceprofile-lorawandeviceprofile.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotwireless-deviceprofile-name"></a>
The name of the new resource\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotwireless-deviceprofile-tags"></a>
The tags are an array of key\-value pairs to attach to the specified resource\. Tags can have a minimum of 0 and a maximum of 50 items\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotwireless-deviceprofile-return-values"></a>

### Ref<a name="aws-resource-iotwireless-deviceprofile-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the device profile ID\.

### Fn::GetAtt<a name="aws-resource-iotwireless-deviceprofile-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotwireless-deviceprofile-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the device profile created\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the device profile created\.