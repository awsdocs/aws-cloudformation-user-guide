# AWS::IoT::TopicRule RepublishActionHeaders<a name="aws-properties-iot-topicrule-republishactionheaders"></a>

Specifies MQTT Version 5\.0 headers information\. For more information, see [MQTT](https://docs.aws.amazon.com/iot/latest/developerguide/mqtt.html) in the IoT Core Developer Guide\.

## Syntax<a name="aws-properties-iot-topicrule-republishactionheaders-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-republishactionheaders-syntax.json"></a>

```
{
  "[ContentType](#cfn-iot-topicrule-republishactionheaders-contenttype)" : String,
  "[CorrelationData](#cfn-iot-topicrule-republishactionheaders-correlationdata)" : String,
  "[MessageExpiry](#cfn-iot-topicrule-republishactionheaders-messageexpiry)" : String,
  "[PayloadFormatIndicator](#cfn-iot-topicrule-republishactionheaders-payloadformatindicator)" : String,
  "[ResponseTopic](#cfn-iot-topicrule-republishactionheaders-responsetopic)" : String,
  "[UserProperties](#cfn-iot-topicrule-republishactionheaders-userproperties)" : [ UserProperty, ... ]
}
```

### YAML<a name="aws-properties-iot-topicrule-republishactionheaders-syntax.yaml"></a>

```
  [ContentType](#cfn-iot-topicrule-republishactionheaders-contenttype): String
  [CorrelationData](#cfn-iot-topicrule-republishactionheaders-correlationdata): String
  [MessageExpiry](#cfn-iot-topicrule-republishactionheaders-messageexpiry): String
  [PayloadFormatIndicator](#cfn-iot-topicrule-republishactionheaders-payloadformatindicator): String
  [ResponseTopic](#cfn-iot-topicrule-republishactionheaders-responsetopic): String
  [UserProperties](#cfn-iot-topicrule-republishactionheaders-userproperties): 
    - UserProperty
```

## Properties<a name="aws-properties-iot-topicrule-republishactionheaders-properties"></a>

`ContentType`  <a name="cfn-iot-topicrule-republishactionheaders-contenttype"></a>
A UTF\-8 encoded string that describes the content of the publishing message\.  
For more information, see [ Content Type](https://docs.oasis-open.org/mqtt/mqtt/v5.0/os/mqtt-v5.0-os.html#_Toc3901118) in the MQTT Version 5\.0 specification\.  
Supports [substitution templates](https://docs.aws.amazon.com/iot/latest/developerguide/iot-substitution-templates.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CorrelationData`  <a name="cfn-iot-topicrule-republishactionheaders-correlationdata"></a>
The base64\-encoded binary data used by the sender of the request message to identify which request the response message is for\.  
For more information, see [ Correlation Data](https://docs.oasis-open.org/mqtt/mqtt/v5.0/os/mqtt-v5.0-os.html#_Toc3901115) in the MQTT Version 5\.0 specification\.  
Supports [substitution templates](https://docs.aws.amazon.com/iot/latest/developerguide/iot-substitution-templates.html)\.  
 This binary data must be base64\-encoded\. 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageExpiry`  <a name="cfn-iot-topicrule-republishactionheaders-messageexpiry"></a>
A user\-defined integer value that represents the message expiry interval at the broker\. If the messages haven't been sent to the subscribers within that interval, the message expires and is removed\. The value of `messageExpiry` represents the number of seconds before it expires\. For more information about the limits of `messageExpiry`, see [Message broker and protocol limits and quotas](https://docs.aws.amazon.com/general/latest/gr/iot-core.html#limits_iot) in the IoT Core Reference Guide\.  
Supports [substitution templates](https://docs.aws.amazon.com/iot/latest/developerguide/iot-substitution-templates.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PayloadFormatIndicator`  <a name="cfn-iot-topicrule-republishactionheaders-payloadformatindicator"></a>
An `Enum` string value that indicates whether the payload is formatted as UTF\-8\.  
Valid values are `UNSPECIFIED_BYTES` and `UTF8_DATA`\.  
For more information, see [ Payload Format Indicator](https://docs.oasis-open.org/mqtt/mqtt/v5.0/os/mqtt-v5.0-os.html#_Toc3901111) from the MQTT Version 5\.0 specification\.  
Supports [substitution templates](https://docs.aws.amazon.com/iot/latest/developerguide/iot-substitution-templates.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseTopic`  <a name="cfn-iot-topicrule-republishactionheaders-responsetopic"></a>
A UTF\-8 encoded string that's used as the topic name for a response message\. The response topic is used to describe the topic to which the receiver should publish as part of the request\-response flow\. The topic must not contain wildcard characters\.  
For more information, see [ Response Topic](https://docs.oasis-open.org/mqtt/mqtt/v5.0/os/mqtt-v5.0-os.html#_Toc3901114) in the MQTT Version 5\.0 specification\.  
Supports [substitution templates](https://docs.aws.amazon.com/iot/latest/developerguide/iot-substitution-templates.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserProperties`  <a name="cfn-iot-topicrule-republishactionheaders-userproperties"></a>
An array of key\-value pairs that you define in the MQTT5 header\.  
*Required*: No  
*Type*: List of [UserProperty](aws-properties-iot-topicrule-userproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)