# AWS::Config::ConfigRule SourceDetail<a name="aws-properties-config-configrule-source-sourcedetails"></a>

Provides the source and the message types that trigger AWS Config to evaluate your AWS resources against a rule\. It also provides the frequency with which you want AWS Config to run evaluations for the rule if the trigger type is periodic\. You can specify the parameter values for `SourceDetail` only for custom rules\. 

## Syntax<a name="aws-properties-config-configrule-source-sourcedetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-configrule-source-sourcedetails-syntax.json"></a>

```
{
  "[EventSource](#cfn-config-configrule-source-sourcedetail-eventsource)" : String,
  "[MaximumExecutionFrequency](#cfn-config-configrule-sourcedetail-maximumexecutionfrequency)" : String,
  "[MessageType](#cfn-config-configrule-source-sourcedetail-messagetype)" : String
}
```

### YAML<a name="aws-properties-config-configrule-source-sourcedetails-syntax.yaml"></a>

```
  [EventSource](#cfn-config-configrule-source-sourcedetail-eventsource): String
  [MaximumExecutionFrequency](#cfn-config-configrule-sourcedetail-maximumexecutionfrequency): String
  [MessageType](#cfn-config-configrule-source-sourcedetail-messagetype): String
```

## Properties<a name="aws-properties-config-configrule-source-sourcedetails-properties"></a>

`EventSource`  <a name="cfn-config-configrule-source-sourcedetail-eventsource"></a>
The source of the event, such as an AWS service, that triggers AWS Config to evaluate your AWS resources\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `aws.config`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumExecutionFrequency`  <a name="cfn-config-configrule-sourcedetail-maximumexecutionfrequency"></a>
The frequency at which you want AWS Config to run evaluations for a custom rule with a periodic trigger\. If you specify a value for `MaximumExecutionFrequency`, then `MessageType` must use the `ScheduledNotification` value\.  
By default, rules with a periodic trigger are evaluated every 24 hours\. To change the frequency, specify a valid value for the `MaximumExecutionFrequency` parameter\.  
Based on the valid value you choose, AWS Config runs evaluations once for each valid value\. For example, if you choose `Three_Hours`, AWS Config runs evaluations once every three hours\. In this case, `Three_Hours` is the frequency of this rule\. 
*Required*: No  
*Type*: String  
*Allowed values*: `One_Hour | Six_Hours | Three_Hours | Twelve_Hours | TwentyFour_Hours`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageType`  <a name="cfn-config-configrule-source-sourcedetail-messagetype"></a>
The type of notification that triggers AWS Config to run an evaluation for a rule\. You can specify the following notification types:  
+  `ConfigurationItemChangeNotification` \- Triggers an evaluation when AWS Config delivers a configuration item as a result of a resource change\.
+  `OversizedConfigurationItemChangeNotification` \- Triggers an evaluation when AWS Config delivers an oversized configuration item\. AWS Config may generate this notification type when a resource changes and the notification exceeds the maximum size allowed by Amazon SNS\.
+  `ScheduledNotification` \- Triggers a periodic evaluation at the frequency specified for `MaximumExecutionFrequency`\.
+  `ConfigurationSnapshotDeliveryCompleted` \- Triggers a periodic evaluation when AWS Config delivers a configuration snapshot\.
If you want your custom rule to be triggered by configuration changes, specify two SourceDetail objects, one for `ConfigurationItemChangeNotification` and one for `OversizedConfigurationItemChangeNotification`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ConfigurationItemChangeNotification | ConfigurationSnapshotDeliveryCompleted | OversizedConfigurationItemChangeNotification | ScheduledNotification`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)