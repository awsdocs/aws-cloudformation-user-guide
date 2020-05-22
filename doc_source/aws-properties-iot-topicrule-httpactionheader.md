# AWS::IoT::TopicRule HttpActionHeader<a name="aws-properties-iot-topicrule-httpactionheader"></a>

The HTTP action header\.

## Syntax<a name="aws-properties-iot-topicrule-httpactionheader-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-httpactionheader-syntax.json"></a>

```
{
  "[Key](#cfn-iot-topicrule-httpactionheader-key)" : String,
  "[Value](#cfn-iot-topicrule-httpactionheader-value)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-httpactionheader-syntax.yaml"></a>

```
  [Key](#cfn-iot-topicrule-httpactionheader-key): String
  [Value](#cfn-iot-topicrule-httpactionheader-value): String
```

## Properties<a name="aws-properties-iot-topicrule-httpactionheader-properties"></a>

`Key`  <a name="cfn-iot-topicrule-httpactionheader-key"></a>
The HTTP header key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-iot-topicrule-httpactionheader-value"></a>
The HTTP header value\. Substitution templates are supported\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)