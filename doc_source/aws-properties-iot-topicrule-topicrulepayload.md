# AWS IoT TopicRule TopicRulePayload<a name="aws-properties-iot-topicrule-topicrulepayload"></a>

`TopicRulePayload` is a property of the `[AWS::IoT::TopicRule](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-topicrule.html)` resource that describes the payload of an AWS IoT rule\.

## Syntax<a name="w3ab2c21c14e1192b5"></a>

### JSON<a name="aws-properties-iot-topicrule-topicrulepayload-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-topicrulepayload-actions)": [ Action, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-topicrulepayload-awsiotsqslversion)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-topicrulepayload-description)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-topicrulepayload-ruledisabled)": Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-topicrulepayload-sql)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-topicrulepayload-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-topicrulepayload-actions):
  - Action
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-topicrulepayload-awsiotsqslversion): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-topicrulepayload-description): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-topicrulepayload-ruledisabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-topicrulepayload-sql): String
```

## Properties<a name="w3ab2c21c14e1192b7"></a>

`Actions`  
The actions associated with the rule\.  
*Required: *Yes  
*Type*: Array of `Action` objects  
*Update requires*: No interruption

`AwsIotSqlVersion`  
The version of the SQL rules engine to use when evaluating the rule\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`Description`  
The description of the rule\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`RuleDisabled`  
Specifies whether the rule is disabled\.  
*Required: *Yes  
*Type*: Boolean  
*Update requires*: No interruption

`Sql`  
The SQL statement that queries the topic\. For more information, see [Rules for AWS IoT](http://docs.aws.amazon.com/iot/latest/developerguide/iot-rules.html#aws-iot-sql-reference) in the *AWS IoT Developer Guide*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption