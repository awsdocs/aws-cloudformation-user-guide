# AWS::IoTWireless::WirelessDevice OtaaV10x<a name="aws-properties-iotwireless-wirelessdevice-otaav10x"></a>

OTAA device object for create APIs for v1\.0\.x\.

## Syntax<a name="aws-properties-iotwireless-wirelessdevice-otaav10x-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-wirelessdevice-otaav10x-syntax.json"></a>

```
{
  "[AppEui](#cfn-iotwireless-wirelessdevice-otaav10x-appeui)" : String,
  "[AppKey](#cfn-iotwireless-wirelessdevice-otaav10x-appkey)" : String
}
```

### YAML<a name="aws-properties-iotwireless-wirelessdevice-otaav10x-syntax.yaml"></a>

```
  [AppEui](#cfn-iotwireless-wirelessdevice-otaav10x-appeui): String
  [AppKey](#cfn-iotwireless-wirelessdevice-otaav10x-appkey): String
```

## Properties<a name="aws-properties-iotwireless-wirelessdevice-otaav10x-properties"></a>

`AppEui`  <a name="cfn-iotwireless-wirelessdevice-otaav10x-appeui"></a>
The AppEUI value, with pattern of `[a-fA-F0-9]{16}`\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-fA-F0-9]{16}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AppKey`  <a name="cfn-iotwireless-wirelessdevice-otaav10x-appkey"></a>
The AppKey is a secret key, which you should handle in a similar way as you would an application password\. You can protect the AppKey value by storing it in the AWS Secrets Manager and use the [secretsmanager](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html#dynamic-references-secretsmanager) to reference this value\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-fA-F0-9]{32}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)