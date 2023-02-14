# AWS::SSMIncidents::ResponsePlan ChatChannel<a name="aws-properties-ssmincidents-responseplan-chatchannel"></a>

The AWS Chatbot chat channel used for collaboration during an incident\.

## Syntax<a name="aws-properties-ssmincidents-responseplan-chatchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmincidents-responseplan-chatchannel-syntax.json"></a>

```
{
  "[ChatbotSns](#cfn-ssmincidents-responseplan-chatchannel-chatbotsns)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ssmincidents-responseplan-chatchannel-syntax.yaml"></a>

```
  [ChatbotSns](#cfn-ssmincidents-responseplan-chatchannel-chatbotsns): 
    - String
```

## Properties<a name="aws-properties-ssmincidents-responseplan-chatchannel-properties"></a>

`ChatbotSns`  <a name="cfn-ssmincidents-responseplan-chatchannel-chatbotsns"></a>
The SNS targets that AWS Chatbot uses to notify the chat channel of updates to an incident\. You can also make updates to the incident through the chat channel by using the SNS topics  
*Required*: No  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)