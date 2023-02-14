# AWS::IoTWireless::WirelessDevice SessionKeysAbpV10x<a name="aws-properties-iotwireless-wirelessdevice-sessionkeysabpv10x"></a>

LoRaWAN object for create APIs\.

## Syntax<a name="aws-properties-iotwireless-wirelessdevice-sessionkeysabpv10x-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-wirelessdevice-sessionkeysabpv10x-syntax.json"></a>

```
{
  "[AppSKey](#cfn-iotwireless-wirelessdevice-sessionkeysabpv10x-appskey)" : String,
  "[NwkSKey](#cfn-iotwireless-wirelessdevice-sessionkeysabpv10x-nwkskey)" : String
}
```

### YAML<a name="aws-properties-iotwireless-wirelessdevice-sessionkeysabpv10x-syntax.yaml"></a>

```
  [AppSKey](#cfn-iotwireless-wirelessdevice-sessionkeysabpv10x-appskey): String
  [NwkSKey](#cfn-iotwireless-wirelessdevice-sessionkeysabpv10x-nwkskey): String
```

## Properties<a name="aws-properties-iotwireless-wirelessdevice-sessionkeysabpv10x-properties"></a>

`AppSKey`  <a name="cfn-iotwireless-wirelessdevice-sessionkeysabpv10x-appskey"></a>
The AppSKey is a secret key, which you should handle in a similar way as you would an application password\. You can protect the AppSKey value by storing it in the AWS Secrets Manager and use the [secretsmanager](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html#dynamic-references-secretsmanager) to reference this value\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-fA-F0-9]{32}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NwkSKey`  <a name="cfn-iotwireless-wirelessdevice-sessionkeysabpv10x-nwkskey"></a>
The NwkSKey is a secret key, which you should handle in a similar way as you would an application password\. You can protect the NwkSKey value by storing it in the AWS Secrets Manager and use the [secretsmanager](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html#dynamic-references-secretsmanager) to reference this value\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-fA-F0-9]{32}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)