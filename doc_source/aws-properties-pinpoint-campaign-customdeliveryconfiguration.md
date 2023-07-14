# AWS::Pinpoint::Campaign CustomDeliveryConfiguration<a name="aws-properties-pinpoint-campaign-customdeliveryconfiguration"></a>

Specifies the delivery configuration settings for sending a campaign or campaign treatment through a custom channel\. This object is required if you use the `CampaignCustomMessage` object to define the message to send for the campaign or campaign treatment\.

## Syntax<a name="aws-properties-pinpoint-campaign-customdeliveryconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-customdeliveryconfiguration-syntax.json"></a>

```
{
  "[DeliveryUri](#cfn-pinpoint-campaign-customdeliveryconfiguration-deliveryuri)" : String,
  "[EndpointTypes](#cfn-pinpoint-campaign-customdeliveryconfiguration-endpointtypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-pinpoint-campaign-customdeliveryconfiguration-syntax.yaml"></a>

```
  [DeliveryUri](#cfn-pinpoint-campaign-customdeliveryconfiguration-deliveryuri): String
  [EndpointTypes](#cfn-pinpoint-campaign-customdeliveryconfiguration-endpointtypes): 
    - String
```

## Properties<a name="aws-properties-pinpoint-campaign-customdeliveryconfiguration-properties"></a>

`DeliveryUri`  <a name="cfn-pinpoint-campaign-customdeliveryconfiguration-deliveryuri"></a>
The destination to send the campaign or treatment to\. This value can be one of the following:  
+ The name or Amazon Resource Name \(ARN\) of an AWS Lambda function to invoke to handle delivery of the campaign or treatment\.
+ The URL for a web application or service that supports HTTPS and can receive the message\. The URL has to be a full URL, including the HTTPS protocol\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointTypes`  <a name="cfn-pinpoint-campaign-customdeliveryconfiguration-endpointtypes"></a>
The types of endpoints to send the campaign or treatment to\. Each valid value maps to a type of channel that you can associate with an endpoint by using the `ChannelType` property of an endpoint\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)