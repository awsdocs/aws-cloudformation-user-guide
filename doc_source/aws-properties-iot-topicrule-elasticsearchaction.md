# AWS IoT TopicRule ElasticsearchAction<a name="aws-properties-iot-topicrule-elasticsearchaction"></a>

`Elasticsearch` is a property of the `Actions` property that describes an action that writes data to an Elasticsearch domain\.

## Syntax<a name="w3ab2c21c14e1144b5"></a>

### JSON<a name="aws-properties-iot-topicrule-elasticsearchaction-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-elasticsearchaction-endpoint)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-elasticsearchaction-id)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-elasticsearchaction-index)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-elasticsearchaction-rolearn)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-elasticsearchaction-type)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-elasticsearchaction-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-elasticsearchaction-endpoint): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-elasticsearchaction-id)": String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-elasticsearchaction-index)": String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-elasticsearchaction-rolearn)": String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-elasticsearchaction-type)": String
```

## Properties<a name="w3ab2c21c14e1144b7"></a>

`Endpoint`  
The endpoint of your Elasticsearch domain\.  
*Required: *Yes  
*Type*: String

`Id`  
A unique identifier for the stored data\.  
*Required: *Yes  
*Type*: String

`Index`  
The Elasticsearch index where the data is stored\.  
*Required: *Yes  
*Type*: String

`RoleArn`  
The ARN of the IAM role that grants access to Elasticsearch\.  
*Required: *Yes  
*Type*: String

`Type`  
The type of stored data\.  
*Required: *Yes  
*Type*: String