# AWS::IoT::TopicRule UserProperty<a name="aws-properties-iot-topicrule-userproperty"></a>

A key\-value pair that you define in the header\.

## Syntax<a name="aws-properties-iot-topicrule-userproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-userproperty-syntax.json"></a>

```
{
  "[Key](#cfn-iot-topicrule-userproperty-key)" : String,
  "[Value](#cfn-iot-topicrule-userproperty-value)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-userproperty-syntax.yaml"></a>

```
  [Key](#cfn-iot-topicrule-userproperty-key): String
  [Value](#cfn-iot-topicrule-userproperty-value): String
```

## Properties<a name="aws-properties-iot-topicrule-userproperty-properties"></a>

`Key`  <a name="cfn-iot-topicrule-userproperty-key"></a>
A key to be specified in `UserProperty`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-iot-topicrule-userproperty-value"></a>
A value to be specified in `UserProperty`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)