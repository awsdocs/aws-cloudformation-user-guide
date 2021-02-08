# AWS::CloudTrail::Trail EventSelector<a name="aws-properties-cloudtrail-trail-eventselector"></a>

Use event selectors to further specify the management and data event settings for your trail\. By default, trails created without specific event selectors will be configured to log all read and write management events, and no data events\. When an event occurs in your account, CloudTrail evaluates the event selector for all trails\. For each trail, if the event matches any event selector, the trail processes and logs the event\. If the event doesn't match any event selector, the trail doesn't log the event\.

You can configure up to five event selectors for a trail\.

You cannot apply both event selectors and advanced event selectors to a trail\.

## Syntax<a name="aws-properties-cloudtrail-trail-eventselector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudtrail-trail-eventselector-syntax.json"></a>

```
{
  "[DataResources](#cfn-cloudtrail-trail-eventselector-dataresources)" : [ DataResource, ... ],
  "[IncludeManagementEvents](#cfn-cloudtrail-trail-eventselector-includemanagementevents)" : Boolean,
  "[ReadWriteType](#cfn-cloudtrail-trail-eventselector-readwritetype)" : String
}
```

### YAML<a name="aws-properties-cloudtrail-trail-eventselector-syntax.yaml"></a>

```
  [DataResources](#cfn-cloudtrail-trail-eventselector-dataresources): 
    - DataResource
  [IncludeManagementEvents](#cfn-cloudtrail-trail-eventselector-includemanagementevents): Boolean
  [ReadWriteType](#cfn-cloudtrail-trail-eventselector-readwritetype): String
```

## Properties<a name="aws-properties-cloudtrail-trail-eventselector-properties"></a>

`DataResources`  <a name="cfn-cloudtrail-trail-eventselector-dataresources"></a>
CloudTrail supports data event logging for Amazon S3 objects and AWS Lambda functions\. You can specify up to 250 resources for an individual event selector, but the total number of data resources cannot exceed 250 across all event selectors in a trail\. This limit does not apply if you configure resource logging for all data events\.   
For more information, see [Data Events](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-management-and-data-events-with-cloudtrail.html#logging-data-events) and [Limits in AWS CloudTrail](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/WhatIsCloudTrail-Limits.html) in the *AWS CloudTrail User Guide*\.  
*Required*: Conditional  
*Type*: List of [DataResource](aws-properties-cloudtrail-trail-dataresource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeManagementEvents`  <a name="cfn-cloudtrail-trail-eventselector-includemanagementevents"></a>
Specify if you want your event selector to include management events for your trail\.  
 For more information, see [Management Events](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-management-and-data-events-with-cloudtrail.html#logging-management-events) in the *AWS CloudTrail User Guide*\.  
By default, the value is `true`\.  
The first copy of management events is free\. You are charged for additional copies of management events that you are logging on any subsequent trail in the same region\. For more information about CloudTrail pricing, see [AWS CloudTrail Pricing](http://aws.amazon.com/cloudtrail/pricing/)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReadWriteType`  <a name="cfn-cloudtrail-trail-eventselector-readwritetype"></a>
Specify if you want your trail to log read\-only events, write\-only events, or all\. For example, the EC2 `GetConsoleOutput` is a read\-only API operation and `RunInstances` is a write\-only API operation\.  
 By default, the value is `All`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `All | ReadOnly | WriteOnly`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)