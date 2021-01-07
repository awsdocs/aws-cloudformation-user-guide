# AWS::IoTWireless::DeviceProfile<a name="aws-resource-iotwireless-deviceprofile"></a>

Creates a new device profile\.

## Syntax<a name="aws-resource-iotwireless-deviceprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotwireless-deviceprofile-syntax.json"></a>

```
{
  "Type" : "AWS::IoTWireless::DeviceProfile",
  "Properties" : {
      "[LoRaWANDeviceProfile](#cfn-iotwireless-deviceprofile-lorawandeviceprofile)" : LoRaWANDeviceProfile,
      "[Name](#cfn-iotwireless-deviceprofile-name)" : String,
      "[NextToken](#cfn-iotwireless-deviceprofile-nexttoken)" : String,
      "[Tags](#cfn-iotwireless-deviceprofile-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotwireless-deviceprofile-syntax.yaml"></a>

```
Type: AWS::IoTWireless::DeviceProfile
Properties: 
  [LoRaWANDeviceProfile](#cfn-iotwireless-deviceprofile-lorawandeviceprofile): 
    LoRaWANDeviceProfile
  [Name](#cfn-iotwireless-deviceprofile-name): String
  [NextToken](#cfn-iotwireless-deviceprofile-nexttoken): String
  [Tags](#cfn-iotwireless-deviceprofile-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotwireless-deviceprofile-properties"></a>

`LoRaWANDeviceProfile`  <a name="cfn-iotwireless-deviceprofile-lorawandeviceprofile"></a>
LoRaWANDeviceProfile object\.  
*Required*: No  
*Type*: [LoRaWANDeviceProfile](aws-properties-iotwireless-deviceprofile-lorawandeviceprofile.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotwireless-deviceprofile-name"></a>
The name of the new resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NextToken`  <a name="cfn-iotwireless-deviceprofile-nexttoken"></a>
This parameter isn't needed to create this resource\. Do not include it in your template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotwireless-deviceprofile-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
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