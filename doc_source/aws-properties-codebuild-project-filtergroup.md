# AWS::CodeBuild::Project FilterGroup<a name="aws-properties-codebuild-project-filtergroup"></a>

A list of `WebhookFilter` objects used to determine which webhook events are triggered\. At least one `WebhookFilter` in the list must specify `EVENT` as its type\. The `FilterGroups` property of the [ AWS CodeBuild Project ProjectTriggers](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-projecttriggers.html) property type is a list of `FilterGroup` objects\.

*Required:* No

*Type:* A list of of [WebhookFilter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-webhookfilter.html) objects

*Update requires:* No interruption

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-east-1`
- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `cn-north-1`
- `cn-northwest-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `me-south-1`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-gov-east-1`
- `us-gov-west-1`
- `us-west-1`
- `us-west-2`
