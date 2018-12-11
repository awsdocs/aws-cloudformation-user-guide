# AWS Config DeliveryChannel ConfigSnapshotDeliveryProperties<a name="aws-properties-config-deliverychannel-configsnapshotdeliveryproperties"></a>

`ConfigSnapshotDeliveryProperties` is a property of the [AWS::Config::DeliveryChannel](aws-resource-config-deliverychannel.md) resource that specifies how AWS Config delivers configuration snapshots to the S3 bucket in your delivery channel\.

## Syntax<a name="w4ab1c21c10c81c29c27b5"></a>

### JSON<a name="aws-properties-config-deliverychannel-configsnapshotdeliveryproperties-syntax.json"></a>

```
{
  "[DeliveryFrequency](#cfn-config-deliverychannel-configsnapshotdeliveryproperties-deliveryfrequency)" : String
}
```

### YAML<a name="aws-properties-config-deliverychannel-configsnapshotdeliveryproperties-syntax.yaml"></a>

```
[DeliveryFrequency](#cfn-config-deliverychannel-configsnapshotdeliveryproperties-deliveryfrequency): String
```

## Properties<a name="w4ab1c21c10c81c29c27b7"></a>

`DeliveryFrequency`  <a name="cfn-config-deliverychannel-configsnapshotdeliveryproperties-deliveryfrequency"></a>
The frequency with which AWS Config delivers configuration snapshots\. For valid values, see [ConfigSnapshotDeliveryProperties](https://docs.aws.amazon.com/config/latest/APIReference/API_ConfigSnapshotDeliveryProperties.html) in the *AWS Config API Reference*\.  
*Required*: No  
*Type*: String