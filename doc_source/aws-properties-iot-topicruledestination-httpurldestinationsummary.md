# AWS::IoT::TopicRuleDestination HttpUrlDestinationSummary<a name="aws-properties-iot-topicruledestination-httpurldestinationsummary"></a>

HTTP URL destination properties\.

## Syntax<a name="aws-properties-iot-topicruledestination-httpurldestinationsummary-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicruledestination-httpurldestinationsummary-syntax.json"></a>

```
{
  "[ConfirmationUrl](#cfn-iot-topicruledestination-httpurldestinationsummary-confirmationurl)" : String
}
```

### YAML<a name="aws-properties-iot-topicruledestination-httpurldestinationsummary-syntax.yaml"></a>

```
  [ConfirmationUrl](#cfn-iot-topicruledestination-httpurldestinationsummary-confirmationurl): String
```

## Properties<a name="aws-properties-iot-topicruledestination-httpurldestinationsummary-properties"></a>

`ConfirmationUrl`  <a name="cfn-iot-topicruledestination-httpurldestinationsummary-confirmationurl"></a>
The URL used to confirm the HTTP topic rule destination URL\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)