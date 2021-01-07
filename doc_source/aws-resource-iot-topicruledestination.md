# AWS::IoT::TopicRuleDestination<a name="aws-resource-iot-topicruledestination"></a>

A topic rule destination\.

## Syntax<a name="aws-resource-iot-topicruledestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-topicruledestination-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::TopicRuleDestination",
  "Properties" : {
      "[HttpUrlProperties](#cfn-iot-topicruledestination-httpurlproperties)" : HttpUrlDestinationSummary,
      "[Status](#cfn-iot-topicruledestination-status)" : String,
      "[VpcProperties](#cfn-iot-topicruledestination-vpcproperties)" : VpcDestinationProperties
    }
}
```

### YAML<a name="aws-resource-iot-topicruledestination-syntax.yaml"></a>

```
Type: AWS::IoT::TopicRuleDestination
Properties: 
  [HttpUrlProperties](#cfn-iot-topicruledestination-httpurlproperties): 
    HttpUrlDestinationSummary
  [Status](#cfn-iot-topicruledestination-status): String
  [VpcProperties](#cfn-iot-topicruledestination-vpcproperties): 
    VpcDestinationProperties
```

## Properties<a name="aws-resource-iot-topicruledestination-properties"></a>

`HttpUrlProperties`  <a name="cfn-iot-topicruledestination-httpurlproperties"></a>
Properties of the HTTP URL\.  
*Required*: No  
*Type*: [HttpUrlDestinationSummary](aws-properties-iot-topicruledestination-httpurldestinationsummary.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Status`  <a name="cfn-iot-topicruledestination-status"></a>  
IN\_PROGRESS  
A topic rule destination was created but has not been confirmed\. You can set status to `IN_PROGRESS` by calling `UpdateTopicRuleDestination`\. Calling `UpdateTopicRuleDestination` causes a new confirmation challenge to be sent to your confirmation endpoint\.  
ENABLED  
Confirmation was completed, and traffic to this destination is allowed\. You can set status to `DISABLED` by calling `UpdateTopicRuleDestination`\.  
DISABLED  
Confirmation was completed, and traffic to this destination is not allowed\. You can set status to `ENABLED` by calling `UpdateTopicRuleDestination`\.  
ERROR  
Confirmation could not be completed, for example if the confirmation timed out\. You can call `GetTopicRuleDestination` for details about the error\. You can set status to `IN_PROGRESS` by calling `UpdateTopicRuleDestination`\. Calling `UpdateTopicRuleDestination` causes a new confirmation challenge to be sent to your confirmation endpoint\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcProperties`  <a name="cfn-iot-topicruledestination-vpcproperties"></a>
Specifies a VPC with the specified IPv4 CIDR block\. The smallest VPC you can create uses a /28 netmask \(16 IPv4 addresses\), and the largest uses a /16 netmask \(65,536 IPv4 addresses\)\.  
*Required*: No  
*Type*: [VpcDestinationProperties](aws-properties-iot-topicruledestination-vpcdestinationproperties.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iot-topicruledestination-return-values"></a>

### Ref<a name="aws-resource-iot-topicruledestination-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the topic rule destination\. For example:

 `{ "Ref": "TopicRuleDestination" }` 

A value similar to the following is returned:

 `a1234567b89c012d3e4fg567hij8k9l01mno1p23q45678901rs234567890t1u2` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iot-topicruledestination-return-values-fn--getatt"></a>



#### <a name="aws-resource-iot-topicruledestination-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The topic rule destination URL\.

`StatusReason`  <a name="StatusReason-fn::getatt"></a>
Additional details or reason why the topic rule destination is in the current status\.