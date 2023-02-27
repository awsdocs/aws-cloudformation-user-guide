# AWS::Connect::Rule NotificationRecipientType<a name="aws-properties-connect-rule-notificationrecipienttype"></a>

The type of notification recipient\.

## Syntax<a name="aws-properties-connect-rule-notificationrecipienttype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-rule-notificationrecipienttype-syntax.json"></a>

```
{
  "[UserArns](#cfn-connect-rule-notificationrecipienttype-userarns)" : [ String, ... ],
  "[UserTags](#cfn-connect-rule-notificationrecipienttype-usertags)" : {Key : Value, ...}
}
```

### YAML<a name="aws-properties-connect-rule-notificationrecipienttype-syntax.yaml"></a>

```
  [UserArns](#cfn-connect-rule-notificationrecipienttype-userarns): 
    - String
  [UserTags](#cfn-connect-rule-notificationrecipienttype-usertags): 
    Key : Value
```

## Properties<a name="aws-properties-connect-rule-notificationrecipienttype-properties"></a>

`UserArns`  <a name="cfn-connect-rule-notificationrecipienttype-userarns"></a>
The Amazon Resource Name \(ARN\) of the user account\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserTags`  <a name="cfn-connect-rule-notificationrecipienttype-usertags"></a>
The tags used to organize, track, or control access for this resource\. For example, \{ "tags": \{"key1":"value1", "key2":"value2"\} \}\. Amazon Connect users with the specified tags will be notified\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)