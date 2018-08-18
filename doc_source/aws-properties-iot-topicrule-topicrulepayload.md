# AWS IoT TopicRule TopicRulePayload<a name="aws-properties-iot-topicrule-topicrulepayload"></a>

`TopicRulePayload` is a property of the `[AWS::IoT::TopicRule](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-topicrule.html)` resource that describes the payload of an AWS IoT rule\.

## Syntax<a name="w3ab2c21c14e1389b5"></a>

### JSON<a name="aws-properties-iot-topicrule-topicrulepayload-syntax.json"></a>

```
{
  "[Actions](#cfn-iot-topicrule-topicrulepayload-actions)": [ Action, ... ],
  "[AwsIotSqlVersion](#cfn-iot-topicrule-topicrulepayload-awsiotsqslversion)": String,
  "[Description](#cfn-iot-topicrule-topicrulepayload-description)": String,
  "[RuleDisabled](#cfn-iot-topicrule-topicrulepayload-ruledisabled)": Boolean,
  "[Sql](#cfn-iot-topicrule-topicrulepayload-sql)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-topicrulepayload-syntax.yaml"></a>

```
[Actions](#cfn-iot-topicrule-topicrulepayload-actions):
  - Action
[AwsIotSqlVersion](#cfn-iot-topicrule-topicrulepayload-awsiotsqslversion): String
[Description](#cfn-iot-topicrule-topicrulepayload-description): String
[RuleDisabled](#cfn-iot-topicrule-topicrulepayload-ruledisabled): Boolean
[Sql](#cfn-iot-topicrule-topicrulepayload-sql): String
```

## Properties<a name="w3ab2c21c14e1389b7"></a>

`Actions`  <a name="cfn-iot-topicrule-topicrulepayload-actions"></a>
The actions associated with the rule\.  
*Required*: Yes  
*Type*: Array of [`Action`](aws-properties-iot-topicrule-action.md) objects  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AwsIotSqlVersion`  <a name="cfn-iot-topicrule-topicrulepayload-awsiotsqslversion"></a>
The version of the SQL rules engine to use when evaluating the rule\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Description`  <a name="cfn-iot-topicrule-topicrulepayload-description"></a>
The description of the rule\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RuleDisabled`  <a name="cfn-iot-topicrule-topicrulepayload-ruledisabled"></a>
Specifies whether the rule is disabled\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Sql`  <a name="cfn-iot-topicrule-topicrulepayload-sql"></a>
The SQL statement that queries the topic\. For more information, see [Rules for AWS IoT](http://docs.aws.amazon.com/iot/latest/developerguide/iot-rules.html#aws-iot-sql-reference) in the *AWS IoT Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)