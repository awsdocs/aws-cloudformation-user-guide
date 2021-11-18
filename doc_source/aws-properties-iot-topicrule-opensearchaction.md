# AWS::IoT::TopicRule OpenSearchAction<a name="aws-properties-iot-topicrule-opensearchaction"></a>

Describes an action that writes data to an Amazon OpenSearch Service domain\.

## Syntax<a name="aws-properties-iot-topicrule-opensearchaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-opensearchaction-syntax.json"></a>

```
{
  "[Endpoint](#cfn-iot-topicrule-opensearchaction-endpoint)" : String,
  "[Id](#cfn-iot-topicrule-opensearchaction-id)" : String,
  "[Index](#cfn-iot-topicrule-opensearchaction-index)" : String,
  "[RoleArn](#cfn-iot-topicrule-opensearchaction-rolearn)" : String,
  "[Type](#cfn-iot-topicrule-opensearchaction-type)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-opensearchaction-syntax.yaml"></a>

```
  [Endpoint](#cfn-iot-topicrule-opensearchaction-endpoint): String
  [Id](#cfn-iot-topicrule-opensearchaction-id): String
  [Index](#cfn-iot-topicrule-opensearchaction-index): String
  [RoleArn](#cfn-iot-topicrule-opensearchaction-rolearn): String
  [Type](#cfn-iot-topicrule-opensearchaction-type): String
```

## Properties<a name="aws-properties-iot-topicrule-opensearchaction-properties"></a>

`Endpoint`  <a name="cfn-iot-topicrule-opensearchaction-endpoint"></a>
The endpoint of your OpenSearch domain\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-iot-topicrule-opensearchaction-id"></a>
The unique identifier for the document you are storing\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Index`  <a name="cfn-iot-topicrule-opensearchaction-index"></a>
The OpenSearch index where you want to store your data\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-opensearchaction-rolearn"></a>
The IAM role ARN that has access to OpenSearch\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-iot-topicrule-opensearchaction-type"></a>
The type of document you are storing\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)