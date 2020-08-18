# AWS::IoT::TopicRule HttpAction<a name="aws-properties-iot-topicrule-httpaction"></a>

Send data to an HTTPS endpoint\.

## Syntax<a name="aws-properties-iot-topicrule-httpaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-httpaction-syntax.json"></a>

```
{
  "[Auth](#cfn-iot-topicrule-httpaction-auth)" : HttpAuthorization,
  "[ConfirmationUrl](#cfn-iot-topicrule-httpaction-confirmationurl)" : String,
  "[Headers](#cfn-iot-topicrule-httpaction-headers)" : [ HttpActionHeader, ... ],
  "[Url](#cfn-iot-topicrule-httpaction-url)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-httpaction-syntax.yaml"></a>

```
  [Auth](#cfn-iot-topicrule-httpaction-auth): 
    HttpAuthorization
  [ConfirmationUrl](#cfn-iot-topicrule-httpaction-confirmationurl): String
  [Headers](#cfn-iot-topicrule-httpaction-headers): 
    - HttpActionHeader
  [Url](#cfn-iot-topicrule-httpaction-url): String
```

## Properties<a name="aws-properties-iot-topicrule-httpaction-properties"></a>

`Auth`  <a name="cfn-iot-topicrule-httpaction-auth"></a>
The authentication method to use when sending data to an HTTPS endpoint\.  
*Required*: No  
*Type*: [HttpAuthorization](aws-properties-iot-topicrule-httpauthorization.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfirmationUrl`  <a name="cfn-iot-topicrule-httpaction-confirmationurl"></a>
The URL to which AWS IoT sends a confirmation message\. The value of the confirmation URL must be a prefix of the endpoint URL\. If you do not specify a confirmation URL AWS IoT uses the endpoint URL as the confirmation URL\. If you use substitution templates in the confirmationUrl, you must create and enable topic rule destinations that match each possible value of the substitution template before traffic is allowed to your endpoint URL\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Headers`  <a name="cfn-iot-topicrule-httpaction-headers"></a>
The HTTP headers to send with the message data\.  
*Required*: No  
*Type*: List of [HttpActionHeader](aws-properties-iot-topicrule-httpactionheader.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-iot-topicrule-httpaction-url"></a>
The endpoint URL\. If substitution templates are used in the URL, you must also specify a `confirmationUrl`\. If this is a new destination, a new `TopicRuleDestination` is created if possible\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)