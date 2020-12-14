# AWS::SES::ReceiptRule WorkmailAction<a name="aws-properties-ses-receiptrule-workmailaction"></a>

When included in a receipt rule, this action calls Amazon WorkMail and, optionally, publishes a notification to Amazon Simple Notification Service \(Amazon SNS\)\. It usually isn't necessary to use this action directly, because Amazon WorkMail adds the rule automatically during its setup procedure\.

For information using a receipt rule to call Amazon WorkMail, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-action-workmail.html)\.

## Syntax<a name="aws-properties-ses-receiptrule-workmailaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-workmailaction-syntax.json"></a>

```
{
  "[OrganizationArn](#cfn-ses-receiptrule-workmailaction-organizationarn)" : String,
  "[TopicArn](#cfn-ses-receiptrule-workmailaction-topicarn)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-workmailaction-syntax.yaml"></a>

```
  [OrganizationArn](#cfn-ses-receiptrule-workmailaction-organizationarn): String
  [TopicArn](#cfn-ses-receiptrule-workmailaction-topicarn): String
```

## Properties<a name="aws-properties-ses-receiptrule-workmailaction-properties"></a>

`OrganizationArn`  <a name="cfn-ses-receiptrule-workmailaction-organizationarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon WorkMail organization\. Amazon WorkMail ARNs use the following format:  
 `arn:aws:workmail:<region>:<awsAccountId>:organization/<workmailOrganizationId>`   
You can find the ID of your organization by using the [ListOrganizations](https://docs.aws.amazon.com/workmail/latest/APIReference/API_ListOrganizations.html) operation in the Amazon WorkMail API\. Amazon WorkMail organization IDs begin with "`m-`", followed by a string of alphanumeric characters\.  
For information about Amazon WorkMail organizations, see the [Amazon WorkMail Administrator Guide](https://docs.aws.amazon.com/workmail/latest/adminguide/organizations_overview.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopicArn`  <a name="cfn-ses-receiptrule-workmailaction-topicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to notify when the WorkMail action is called\. You can find the ARN of a topic by using the [ListTopics](https://docs.aws.amazon.com/sns/latest/api/API_ListTopics.html) operation in the Amazon SNS API\.  
For more information about Amazon SNS topics, see the [Amazon SNS Developer Guide](https://docs.aws.amazon.com/sns/latest/dg/CreateTopic.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)