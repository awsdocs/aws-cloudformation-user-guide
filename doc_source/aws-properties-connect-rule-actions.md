# AWS::Connect::Rule Actions<a name="aws-properties-connect-rule-actions"></a>

 A list of actions to be run when the rule is triggered\.

## Syntax<a name="aws-properties-connect-rule-actions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-rule-actions-syntax.json"></a>

```
{
  "[AssignContactCategoryActions](#cfn-connect-rule-actions-assigncontactcategoryactions)" : [ Json, ... ],
  "[EventBridgeActions](#cfn-connect-rule-actions-eventbridgeactions)" : [ EventBridgeAction, ... ],
  "[SendNotificationActions](#cfn-connect-rule-actions-sendnotificationactions)" : [ SendNotificationAction, ... ],
  "[TaskActions](#cfn-connect-rule-actions-taskactions)" : [ TaskAction, ... ]
}
```

### YAML<a name="aws-properties-connect-rule-actions-syntax.yaml"></a>

```
  [AssignContactCategoryActions](#cfn-connect-rule-actions-assigncontactcategoryactions): 
    - Json
  [EventBridgeActions](#cfn-connect-rule-actions-eventbridgeactions): 
    - EventBridgeAction
  [SendNotificationActions](#cfn-connect-rule-actions-sendnotificationactions): 
    - SendNotificationAction
  [TaskActions](#cfn-connect-rule-actions-taskactions): 
    - TaskAction
```

## Properties<a name="aws-properties-connect-rule-actions-properties"></a>

`AssignContactCategoryActions`  <a name="cfn-connect-rule-actions-assigncontactcategoryactions"></a>
Information about the contact category action\. The syntax can be empty, for example, `{}`\.  
*Required*: No  
*Type*: List of Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventBridgeActions`  <a name="cfn-connect-rule-actions-eventbridgeactions"></a>
Information about the EventBridge action\.  
*Required*: No  
*Type*: List of [EventBridgeAction](aws-properties-connect-rule-eventbridgeaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SendNotificationActions`  <a name="cfn-connect-rule-actions-sendnotificationactions"></a>
Information about the send notification action\.  
*Required*: No  
*Type*: List of [SendNotificationAction](aws-properties-connect-rule-sendnotificationaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskActions`  <a name="cfn-connect-rule-actions-taskactions"></a>
Information about the task action\. This field is required if `TriggerEventSource` is one of the following values: `OnZendeskTicketCreate` \| `OnZendeskTicketStatusUpdate` \| `OnSalesforceCaseCreate`  
*Required*: No  
*Type*: List of [TaskAction](aws-properties-connect-rule-taskaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)