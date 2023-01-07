# AWS::IoT::TopicRule PutItemInput<a name="aws-properties-iot-topicrule-putiteminput"></a>

The input for the DynamoActionVS action that specifies the DynamoDB table to which the message data will be written\.

## Syntax<a name="aws-properties-iot-topicrule-putiteminput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-putiteminput-syntax.json"></a>

```
{
  "[TableName](#cfn-iot-topicrule-putiteminput-tablename)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-putiteminput-syntax.yaml"></a>

```
  [TableName](#cfn-iot-topicrule-putiteminput-tablename): String
```

## Properties<a name="aws-properties-iot-topicrule-putiteminput-properties"></a>

`TableName`  <a name="cfn-iot-topicrule-putiteminput-tablename"></a>
The table where the message data will be written\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)