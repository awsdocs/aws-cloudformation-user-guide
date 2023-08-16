# AWS::CodeBuild::Project FilterGroup<a name="aws-properties-codebuild-project-filtergroup"></a>

A list of `WebhookFilter` objects used to determine which webhook events are triggered\. At least one `WebhookFilter` in the list must specify `EVENT` as its type\. The `FilterGroups` property of the [AWS CodeBuild Project ProjectTriggers](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-projecttriggers.html) property type is a list of `FilterGroup` objects\.

**Note**  
The Webhook feature isn't available in AWS CloudFormation for GitHub Enterprise projects\. Use the AWS CLI or AWS CodeBuild console to create the webhook\.

*Required:* No

*Type:* A list of [WebhookFilter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-webhookfilter.html) objects

*Update requires:* No interruption