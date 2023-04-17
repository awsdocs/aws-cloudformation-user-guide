# AWS::OpenSearchService::Domain WindowStartTime<a name="aws-properties-opensearchservice-domain-windowstarttime"></a>

A custom start time for the off\-peak window, in Coordinated Universal Time \(UTC\)\. The window length will always be 10 hours, so you can't specify an end time\. For example, if you specify 11:00 P\.M\. UTC as a start time, the end time will automatically be set to 9:00 A\.M\.

## Syntax<a name="aws-properties-opensearchservice-domain-windowstarttime-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchservice-domain-windowstarttime-syntax.json"></a>

```
{
  "[Hours](#cfn-opensearchservice-domain-windowstarttime-hours)" : Integer,
  "[Minutes](#cfn-opensearchservice-domain-windowstarttime-minutes)" : Integer
}
```

### YAML<a name="aws-properties-opensearchservice-domain-windowstarttime-syntax.yaml"></a>

```
  [Hours](#cfn-opensearchservice-domain-windowstarttime-hours): Integer
  [Minutes](#cfn-opensearchservice-domain-windowstarttime-minutes): Integer
```

## Properties<a name="aws-properties-opensearchservice-domain-windowstarttime-properties"></a>

`Hours`  <a name="cfn-opensearchservice-domain-windowstarttime-hours"></a>
The start hour of the window in Coordinated Universal Time \(UTC\), using 24\-hour time\. For example, 17 refers to 5:00 P\.M\. UTC\. The minimum value is 0 and the maximum value is 23\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Minutes`  <a name="cfn-opensearchservice-domain-windowstarttime-minutes"></a>
The start minute of the window, in UTC\. The minimum value is 0 and the maximum value is 59\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)