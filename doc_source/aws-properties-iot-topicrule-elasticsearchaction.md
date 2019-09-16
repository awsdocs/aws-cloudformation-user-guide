# AWS::IoT::TopicRule ElasticsearchAction<a name="aws-properties-iot-topicrule-elasticsearchaction"></a>

Describes an action that writes data to an Amazon Elasticsearch Service domain\.

## Syntax<a name="aws-properties-iot-topicrule-elasticsearchaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-elasticsearchaction-syntax.json"></a>

```
{
  "[Endpoint](#cfn-iot-topicrule-elasticsearchaction-endpoint)" : String,
  "[Id](#cfn-iot-topicrule-elasticsearchaction-id)" : String,
  "[Index](#cfn-iot-topicrule-elasticsearchaction-index)" : String,
  "[RoleArn](#cfn-iot-topicrule-elasticsearchaction-rolearn)" : String,
  "[Type](#cfn-iot-topicrule-elasticsearchaction-type)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-elasticsearchaction-syntax.yaml"></a>

```
  [Endpoint](#cfn-iot-topicrule-elasticsearchaction-endpoint): String
  [Id](#cfn-iot-topicrule-elasticsearchaction-id): String
  [Index](#cfn-iot-topicrule-elasticsearchaction-index): String
  [RoleArn](#cfn-iot-topicrule-elasticsearchaction-rolearn): String
  [Type](#cfn-iot-topicrule-elasticsearchaction-type): String
```

## Properties<a name="aws-properties-iot-topicrule-elasticsearchaction-properties"></a>

`Endpoint`  <a name="cfn-iot-topicrule-elasticsearchaction-endpoint"></a>
The endpoint of your Elasticsearch domain\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-iot-topicrule-elasticsearchaction-id"></a>
The unique identifier for the document you are storing\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Index`  <a name="cfn-iot-topicrule-elasticsearchaction-index"></a>
The Elasticsearch index where you want to store your data\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-elasticsearchaction-rolearn"></a>
The IAM role ARN that has access to Elasticsearch\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-iot-topicrule-elasticsearchaction-type"></a>
The type of document you are storing\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)