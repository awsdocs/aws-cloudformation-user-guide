# AWS::CloudTrail::EventDataStore AdvancedEventSelector<a name="aws-properties-cloudtrail-eventdatastore-advancedeventselector"></a>

Advanced event selectors let you create fine\-grained selectors for the following AWS CloudTrail event record ﬁelds\. They help you control costs by logging only those events that are important to you\. For more information about advanced event selectors, see [Logging data events](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-data-events-with-cloudtrail.html) in the * AWS CloudTrail User Guide*\.
+  `readOnly` 
+  `eventSource` 
+  `eventName` 
+  `eventCategory` 
+  `resources.type` 
+  `resources.ARN` 

You cannot apply both event selectors and advanced event selectors to a trail\.

## Syntax<a name="aws-properties-cloudtrail-eventdatastore-advancedeventselector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudtrail-eventdatastore-advancedeventselector-syntax.json"></a>

```
{
  "[FieldSelectors](#cfn-cloudtrail-eventdatastore-advancedeventselector-fieldselectors)" : [ AdvancedFieldSelector, ... ],
  "[Name](#cfn-cloudtrail-eventdatastore-advancedeventselector-name)" : String
}
```

### YAML<a name="aws-properties-cloudtrail-eventdatastore-advancedeventselector-syntax.yaml"></a>

```
  [FieldSelectors](#cfn-cloudtrail-eventdatastore-advancedeventselector-fieldselectors): 
    - AdvancedFieldSelector
  [Name](#cfn-cloudtrail-eventdatastore-advancedeventselector-name): String
```

## Properties<a name="aws-properties-cloudtrail-eventdatastore-advancedeventselector-properties"></a>

`FieldSelectors`  <a name="cfn-cloudtrail-eventdatastore-advancedeventselector-fieldselectors"></a>
Contains all selector statements in an advanced event selector\.  
*Required*: Yes  
*Type*: List of [AdvancedFieldSelector](aws-properties-cloudtrail-eventdatastore-advancedfieldselector.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudtrail-eventdatastore-advancedeventselector-name"></a>
An optional, descriptive name for an advanced event selector, such as "Log data events for only two S3 buckets"\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1000`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)