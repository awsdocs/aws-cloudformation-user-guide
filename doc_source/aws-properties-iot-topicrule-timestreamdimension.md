# AWS::IoT::TopicRule TimestreamDimension<a name="aws-properties-iot-topicrule-timestreamdimension"></a>

Metadata attributes of the time series that are written in each measure record\. 

## Syntax<a name="aws-properties-iot-topicrule-timestreamdimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-timestreamdimension-syntax.json"></a>

```
{
  "[Name](#cfn-iot-topicrule-timestreamdimension-name)" : String,
  "[Value](#cfn-iot-topicrule-timestreamdimension-value)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-timestreamdimension-syntax.yaml"></a>

```
  [Name](#cfn-iot-topicrule-timestreamdimension-name): String
  [Value](#cfn-iot-topicrule-timestreamdimension-value): String
```

## Properties<a name="aws-properties-iot-topicrule-timestreamdimension-properties"></a>

`Name`  <a name="cfn-iot-topicrule-timestreamdimension-name"></a>
The metadata dimension name\. This is the name of the column in the database table record\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-iot-topicrule-timestreamdimension-value"></a>
The value to write in this column of the database record\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)