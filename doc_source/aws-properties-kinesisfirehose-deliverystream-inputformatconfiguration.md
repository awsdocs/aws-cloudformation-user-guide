# AWS::KinesisFirehose::DeliveryStream InputFormatConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-inputformatconfiguration"></a>

Specifies the deserializer you want to use to convert the format of the input data\. This parameter is required if `Enabled` is set to true\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-inputformatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-inputformatconfiguration-syntax.json"></a>

```
{
  "[Deserializer](#cfn-kinesisfirehose-deliverystream-inputformatconfiguration-deserializer)" : Deserializer
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-inputformatconfiguration-syntax.yaml"></a>

```
  [Deserializer](#cfn-kinesisfirehose-deliverystream-inputformatconfiguration-deserializer): 
    Deserializer
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-inputformatconfiguration-properties"></a>

`Deserializer`  <a name="cfn-kinesisfirehose-deliverystream-inputformatconfiguration-deserializer"></a>
Specifies which deserializer to use\. You can choose either the Apache Hive JSON SerDe or the OpenX JSON SerDe\. If both are non\-null, the server rejects the request\.  
*Required*: No  
*Type*: [Deserializer](aws-properties-kinesisfirehose-deliverystream-deserializer.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)