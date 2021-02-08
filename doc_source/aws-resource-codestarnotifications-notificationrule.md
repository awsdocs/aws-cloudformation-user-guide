# AWS::CodeStarNotifications::NotificationRule<a name="aws-resource-codestarnotifications-notificationrule"></a>

Creates a notification rule for a resource\. The rule specifies the events you want notifications about and the targets \(such as Amazon SNS topics or AWS Chatbot clients configured for Slack\) where you want to receive them\.

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
      "[Targets](#cfn-codestarnotifications-notificationrule-targets)" : [ Target, ... ]
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
    - Target
```

## Properties<a name="aws-resource-codestarnotifications-notificationrule-properties"></a>

`DetailType`  <a name="cfn-codestarnotifications-notificationrule-detailtype"></a>
The level of detail to include in the notifications for this resource\. BASIC will include only the contents of the event as it would appear in AWS CloudWatch\. FULL will include any supplemental information provided by AWS CodeStar Notifications and/or the service for the resource for which the notification is created\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `BASIC | FULL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventTypeIds`  <a name="cfn-codestarnotifications-notificationrule-eventtypeids"></a>
A list of event types associated with this notification rule\. For a complete list of event types and IDs, see [Notification concepts](https://docs.aws.amazon.com/codestar-notifications/latest/userguide/concepts.html#concepts-api) in the *Developer Tools Console User Guide*\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-codestarnotifications-notificationrule-name"></a>
The name for the notification rule\. Notification rule names must be unique in your AWS account\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[A-Za-z0-9\-_ ]+$`  
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
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-codestarnotifications-notificationrule-tags"></a>
A list of tags to apply to this notification rule\. Key names cannot start with "aws"\.   
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Targets`  <a name="cfn-codestarnotifications-notificationrule-targets"></a>
A list of Amazon Resource Names \(ARNs\) of Amazon SNS topics and AWS Chatbot clients to associate with the notification rule\.  
*Required*: Yes  
*Type*: List of [Target](aws-properties-codestarnotifications-notificationrule-target.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-codestarnotifications-notificationrule-return-values"></a>

### Ref<a name="aws-resource-codestarnotifications-notificationrule-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, `Ref` returns the notification rule ARN\. 

## Examples<a name="aws-resource-codestarnotifications-notificationrule--examples"></a>



### Example<a name="aws-resource-codestarnotifications-notificationrule--examples--Example"></a>

The following example creates a notification rule with a name of My Notification Rule for Comments on Commits\. The notification rule is tagged with a key\-value pair indicating what team owns the rule\.

#### JSON<a name="aws-resource-codestarnotifications-notificationrule--examples--Example--json"></a>

```
{
    "Type": "AWS::CodeStarNotifications::NotificationRule",
    "Properties": {
        "Name": "My Notification Rule for Comments on Commits",
        "DetailType": "FULL",
        "Resource": "arn:aws:codecommit:us-east-2:123456789012:MyDemoRepo",
        "EventTypeIds": [
            "codecommit-repository-comments-on-commits"
        ],
        "Targets": [
            {
                "TargetType": "SNS",
                "TargetAddress": "arn:aws:sns:us-east-2:123456789012:MyNotificationTopic"
            }
        ],
        "Tags": {
            "Team": "Saanvi"
         }
     }
}
```

#### YAML<a name="aws-resource-codestarnotifications-notificationrule--examples--Example--yaml"></a>

```
Type: 'AWS::CodeStarNotifications::NotificationRule'
Properties:
        Name: 'My Notification Rule for Comments on Commits'
        DetailType: FULL
        Resource: 'arn:aws:codecommit:us-east-2:123456789012:MyDemoRepo'
        EventTypeIds: 
            - codecommit-repository-comments-on-commits
        Targets: 
            - TargetType: SNS 
              TargetAddress: 'arn:aws:sns:us-east-2:123456789012:MyNotificationTopic'
        Tags: 
             Team: Saanvi
```