# AWS::KinesisFirehose::DeliveryStream HttpEndpointCommonAttribute<a name="aws-properties-kinesisfirehose-deliverystream-httpendpointcommonattribute"></a>

Describes the metadata that's delivered to the specified HTTP endpoint destination\. Kinesis Firehose supports any custom HTTP endpoint or HTTP endpoints owned by supported third\-party service providers, including Datadog, MongoDB, and New Relic\. 

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-httpendpointcommonattribute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-httpendpointcommonattribute-syntax.json"></a>

```
{
  "[AttributeName](#cfn-kinesisfirehose-deliverystream-httpendpointcommonattribute-attributename)" : String,
  "[AttributeValue](#cfn-kinesisfirehose-deliverystream-httpendpointcommonattribute-attributevalue)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-httpendpointcommonattribute-syntax.yaml"></a>

```
  [AttributeName](#cfn-kinesisfirehose-deliverystream-httpendpointcommonattribute-attributename): String
  [AttributeValue](#cfn-kinesisfirehose-deliverystream-httpendpointcommonattribute-attributevalue): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-httpendpointcommonattribute-properties"></a>

`AttributeName`  <a name="cfn-kinesisfirehose-deliverystream-httpendpointcommonattribute-attributename"></a>
The name of the HTTP endpoint common attribute\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^(?!\s*$).+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AttributeValue`  <a name="cfn-kinesisfirehose-deliverystream-httpendpointcommonattribute-attributevalue"></a>
The value of the HTTP endpoint common attribute\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)