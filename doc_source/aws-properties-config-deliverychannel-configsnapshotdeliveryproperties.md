# AWS::Config::DeliveryChannel ConfigSnapshotDeliveryProperties<a name="aws-properties-config-deliverychannel-configsnapshotdeliveryproperties"></a>

Provides options for how often AWS Config delivers configuration snapshots to the Amazon S3 bucket in your delivery channel\.

**Note**  
If you want to create a rule that triggers evaluations for your resources when AWS Config delivers the configuration snapshot, see the following:

The frequency for a rule that triggers evaluations for your resources when AWS Config delivers the configuration snapshot is set by one of two values, depending on which is less frequent:
+ The value for the `deliveryFrequency` parameter within the delivery channel configuration, which sets how often AWS Config delivers configuration snapshots\. This value also sets how often AWS Config invokes evaluations for AWS Config rules\.
+ The value for the `MaximumExecutionFrequency` parameter, which sets the maximum frequency with which AWS Config invokes evaluations for the rule\. For more information, see [ConfigRule](https://docs.aws.amazon.com/config/latest/APIReference/API_ConfigRule.html)\.

If the `deliveryFrequency` value is less frequent than the `MaximumExecutionFrequency` value for a rule, AWS Config invokes the rule only as often as the `deliveryFrequency` value\.

1. For example, you want your rule to run evaluations when AWS Config delivers the configuration snapshot\.

1. You specify the `MaximumExecutionFrequency` value for `Six_Hours`\. 

1. You then specify the delivery channel `deliveryFrequency` value for `TwentyFour_Hours`\.

1. Because the value for `deliveryFrequency` is less frequent than `MaximumExecutionFrequency`, AWS Config invokes evaluations for the rule every 24 hours\. 

You should set the `MaximumExecutionFrequency` value to be at least as frequent as the `deliveryFrequency` value\. You can view the `deliveryFrequency` value by using the `DescribeDeliveryChannnels` action\.

To update the `deliveryFrequency` with which AWS Config delivers your configuration snapshots, use the `PutDeliveryChannel` action\.

## Syntax<a name="aws-properties-config-deliverychannel-configsnapshotdeliveryproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-config-deliverychannel-configsnapshotdeliveryproperties-properties"></a>

`DeliveryFrequency`  <a name="cfn-config-deliverychannel-configsnapshotdeliveryproperties-deliveryfrequency"></a>
The frequency with which AWS Config delivers configuration snapshots\.  
*Required*: No  
*Type*: String  
*Allowed values*: `One_Hour | Six_Hours | Three_Hours | Twelve_Hours | TwentyFour_Hours`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)