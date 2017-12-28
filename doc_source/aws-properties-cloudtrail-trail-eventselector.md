# AWS CloudTrail Trail EventSelector<a name="aws-properties-cloudtrail-trail-eventselector"></a>

The `EventSelector` property type configures logging of management events and data events for an AWS CloudTrail trail\. For more information, see [PutEventSelectors](http://docs.aws.amazon.com/awscloudtrail/latest/APIReference/API_PutEventSelectors.html) in the *AWS CloudTrail API Reference*\.

 `EventSelector` is a property of the [AWS::CloudTrail::Trail](aws-resource-cloudtrail-trail.md) resource\. 

## Syntax<a name="aws-properties-cloudtrail-trail-eventselector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudtrail-trail-eventselector-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-eventselector-dataresources)" : [ DataResource, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-eventselector-includemanagementevents)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-eventselector-readwritetype)" : String
}
```

### YAML<a name="aws-properties-cloudtrail-trail-eventselector-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-eventselector-dataresources): 
  - DataResource
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-eventselector-includemanagementevents): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-eventselector-readwritetype): String
```

## Properties<a name="aws-properties-cloudtrail-trail-eventselector-properties"></a>

`DataResources`  
The resources for data events\. CloudTrail supports logging data events for Amazon S3 objects only\. For more information, see [Data Events](http://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-management-and-data-events-with-cloudtrail.html#logging-data-events) in the *AWS CloudTrail User Guide*\.  
 *Required*: No  
 *Type*: List of [CloudTrail Trail DataResource](aws-properties-cloudtrail-trail-dataresource.md)  
 *Update requires*: No interruption 

`IncludeManagementEvents`  
Specifies whether the event selector includes management events for the trail\. The default value is `true`\. For more information, see [Management Events](http://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-management-and-data-events-with-cloudtrail.html#logging-management-events) in the *AWS CloudTrail User Guide*\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: No interruption 

`ReadWriteType`  
Specifies whether to log read\-only events, write\-only events, or all events\. The default value is `All`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 