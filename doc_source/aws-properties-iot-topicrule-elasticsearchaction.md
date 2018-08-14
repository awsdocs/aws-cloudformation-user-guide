# AWS IoT TopicRule ElasticsearchAction<a name="aws-properties-iot-topicrule-elasticsearchaction"></a>

`Elasticsearch` is a property of the `Actions` property that describes an action that writes data to an Elasticsearch domain\.

## Syntax<a name="w3ab2c21c14e1341b5"></a>

### JSON<a name="aws-properties-iot-topicrule-elasticsearchaction-syntax.json"></a>

```
{
  "[Endpoint](#cfn-iot-topicrule-elasticsearchaction-endpoint)": String,
  "[Id](#cfn-iot-topicrule-elasticsearchaction-id)": String,
  "[Index](#cfn-iot-topicrule-elasticsearchaction-index)": String,
  "[RoleArn](#cfn-iot-topicrule-elasticsearchaction-rolearn)": String,
  "[Type](#cfn-iot-topicrule-elasticsearchaction-type)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-elasticsearchaction-syntax.yaml"></a>

```
[Endpoint](#cfn-iot-topicrule-elasticsearchaction-endpoint): String
[Id](#cfn-iot-topicrule-elasticsearchaction-id)": String
[Index](#cfn-iot-topicrule-elasticsearchaction-index)": String
[RoleArn](#cfn-iot-topicrule-elasticsearchaction-rolearn)": String
[Type](#cfn-iot-topicrule-elasticsearchaction-type)": String
```

## Properties<a name="w3ab2c21c14e1341b7"></a>

`Endpoint`  <a name="cfn-iot-topicrule-elasticsearchaction-endpoint"></a>
The endpoint of your Elasticsearch domain\.  
*Required*: Yes  
*Type*: String

`Id`  <a name="cfn-iot-topicrule-elasticsearchaction-id"></a>
A unique identifier for the stored data\.  
*Required*: Yes  
*Type*: String

`Index`  <a name="cfn-iot-topicrule-elasticsearchaction-index"></a>
The Elasticsearch index where the data is stored\.  
*Required*: Yes  
*Type*: String

`RoleArn`  <a name="cfn-iot-topicrule-elasticsearchaction-rolearn"></a>
The ARN of the IAM role that grants access to Elasticsearch\.  
*Required*: Yes  
*Type*: String

`Type`  <a name="cfn-iot-topicrule-elasticsearchaction-type"></a>
The type of stored data\.  
*Required*: Yes  
*Type*: String