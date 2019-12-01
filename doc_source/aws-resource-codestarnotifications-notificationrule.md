# AWS::CodeStarNotifications::NotificationRule<a name="aws-resource-codestarnotifications-notificationrule"></a>

Creates a notification rule for a resource\. The rule specifies the events you want notifications about and the targets \(such as SNS topics\) where you want to receive them\.

## Syntax<a name="aws-resource-codestarnotifications-notificationrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codestarnotifications-notificationrule-syntax.json"></a>

```
{
  "Type" : "AWS::CodeStarNotifications::NotificationRule",
  "Properties" : {
      "[DetailType](#cfn-codestarnotifications-notificationrule-detailtype)" : String,
      "[EventTypeIds](#cfn-codestarnotifications-notificationrule-eventtypeids)" : [ String, ... ],
      "[Name](#cfn-codestarnotifications-notificationrule-name)" : String,
      "[Resource](#cfn-codestarnotifications-notificationrule-resource)" : String,
      "[Status](#cfn-codestarnotifications-notificationrule-status)" : String,
      "[Tags](#cfn-codestarnotifications-notificationrule-tags)" : Json,
      "[Targets](#cfn-codestarnotifications-notificationrule-targets)" : [ [Target](aws-properties-codestarnotifications-notificationrule-target.md), ... ]
    }
}
```

### YAML<a name="aws-resource-codestarnotifications-notificationrule-syntax.yaml"></a>

```
Type: AWS::CodeStarNotifications::NotificationRule
Properties: 
  [DetailType](#cfn-codestarnotifications-notificationrule-detailtype): String
  [EventTypeIds](#cfn-codestarnotifications-notificationrule-eventtypeids): 
    - String
  [Name](#cfn-codestarnotifications-notificationrule-name): String
  [Resource](#cfn-codestarnotifications-notificationrule-resource): String
  [Status](#cfn-codestarnotifications-notificationrule-status): String
  [Tags](#cfn-codestarnotifications-notificationrule-tags): Json
  [Targets](#cfn-codestarnotifications-notificationrule-targets): 
    - [Target](aws-properties-codestarnotifications-notificationrule-target.md)
```

## Properties<a name="aws-resource-codestarnotifications-notificationrule-properties"></a>

`DetailType`  <a name="cfn-codestarnotifications-notificationrule-detailtype"></a>
The level of detail to include in the notifications for this resource\. BASIC will include only the contents of the event as it would appear in AWS CloudWatch\. FULL will include any supplemental information provided by AWS CodeStar Notifications and/or the service for the resource for which the notification is created\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `BASIC | FULL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventTypeIds`  <a name="cfn-codestarnotifications-notificationrule-eventtypeids"></a>
A list of event types associated with this notification rule\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-codestarnotifications-notificationrule-name"></a>
The name of the attribute you want to use to filter the returned notification rules\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `CREATED_BY | EVENT_TYPE_ID | RESOURCE | TARGET_ADDRESS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Resource`  <a name="cfn-codestarnotifications-notificationrule-resource"></a>
The Amazon Resource Name \(ARN\) of the resource to associate with the notification rule\. Supported resources include pipelines in AWS CodePipeline, repositories in AWS CodeCommit, and build projects in AWS CodeBuild\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^arn:aws[^:\s]*:[^:\s]*:[^:\s]*:[0-9]{12}:[^\s]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Status`  <a name="cfn-codestarnotifications-notificationrule-status"></a>
The status of the notification rule\. The default value is ENABLED\. If the status is set to DISABLED, notifications aren't sent for the notification rule\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-codestarnotifications-notificationrule-tags"></a>
A list of tags to apply to this notification rule\. Key names cannot start with "aws"\.   
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Targets`  <a name="cfn-codestarnotifications-notificationrule-targets"></a>
A list of Amazon Resource Names \(ARNs\) of SNS topics to associate with the notification rule\.  
*Required*: Yes  
*Type*: List of [Target](aws-properties-codestarnotifications-notificationrule-target.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-codestarnotifications-notificationrule-return-values"></a>

### Ref<a name="aws-resource-codestarnotifications-notificationrule-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, `Ref` returns the notification rule ARN\. 