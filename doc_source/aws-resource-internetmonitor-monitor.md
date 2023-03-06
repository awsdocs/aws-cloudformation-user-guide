# AWS::InternetMonitor::Monitor<a name="aws-resource-internetmonitor-monitor"></a>

The `AWS::InternetMonitor::Monitor` resource is an Internet Monitor resource type that contains information about how you create a monitor in Amazon CloudWatch Internet Monitor\. A monitor in Internet Monitor provides visibility into performance and availability between your applications hosted on AWS and your end users, using a traffic profile that it creates based on the application resources that you add: Virtual Private Clouds \(VPCs\), Amazon CloudFront distributions, or WorkSpaces directories\. 

Internet Monitor also alerts you to internet issues that impact your application in the city\-networks \(geographies and networks\) where your end users use it\. With Internet Monitor, you can quickly pinpoint the locations and providers that are affected, so that you can address the issue\.

For more information, see [ Using Amazon CloudWatch Internet Monitor](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-InternetMonitor.html) in the *Amazon CloudWatch User Guide*\.

## Syntax<a name="aws-resource-internetmonitor-monitor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-internetmonitor-monitor-syntax.json"></a>

```
{
  "Type" : "AWS::InternetMonitor::Monitor",
  "Properties" : {
      "[MaxCityNetworksToMonitor](#cfn-internetmonitor-monitor-maxcitynetworkstomonitor)" : Integer,
      "[MonitorName](#cfn-internetmonitor-monitor-monitorname)" : String,
      "[Resources](#cfn-internetmonitor-monitor-resources)" : [ String, ... ],
      "[ResourcesToAdd](#cfn-internetmonitor-monitor-resourcestoadd)" : [ String, ... ],
      "[ResourcesToRemove](#cfn-internetmonitor-monitor-resourcestoremove)" : [ String, ... ],
      "[Status](#cfn-internetmonitor-monitor-status)" : String,
      "[Tags](#cfn-internetmonitor-monitor-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-internetmonitor-monitor-syntax.yaml"></a>

```
Type: AWS::InternetMonitor::Monitor
Properties: 
  [MaxCityNetworksToMonitor](#cfn-internetmonitor-monitor-maxcitynetworkstomonitor): Integer
  [MonitorName](#cfn-internetmonitor-monitor-monitorname): String
  [Resources](#cfn-internetmonitor-monitor-resources): 
    - String
  [ResourcesToAdd](#cfn-internetmonitor-monitor-resourcestoadd): 
    - String
  [ResourcesToRemove](#cfn-internetmonitor-monitor-resourcestoremove): 
    - String
  [Status](#cfn-internetmonitor-monitor-status): String
  [Tags](#cfn-internetmonitor-monitor-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-internetmonitor-monitor-properties"></a>

`MaxCityNetworksToMonitor`  <a name="cfn-internetmonitor-monitor-maxcitynetworkstomonitor"></a>
The maximum number of city\-networks to monitor for your resources\. A city\-network is the location \(city\) where clients access your application resources from and the network, such as an internet service provider, that clients access the resources through\.  
For more information, see [ Choosing a city\-network maximum value](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/IMCityNetworksMaximum.html) in *Using Amazon CloudWatch Internet Monitor*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitorName`  <a name="cfn-internetmonitor-monitor-monitorname"></a>
The name of the monitor\. A monitor name can contain only alphanumeric characters, dashes \(\-\), periods \(\.\), and underscores \(\_\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Resources`  <a name="cfn-internetmonitor-monitor-resources"></a>
The resources that have been added for the monitor, listed by their Amazon Resource Names \(ARNs\)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourcesToAdd`  <a name="cfn-internetmonitor-monitor-resourcestoadd"></a>
The resources to add to a monitor, which you provide as a set of Amazon Resource Names \(ARNs\)\.  
You can add a combination of Virtual Private Clouds \(VPCs\) and Amazon CloudFront distributions, or you can add WorkSpaces directories\. You can't add all three types of resources\.  
If you add only VPC resources, at least one VPC must have an Internet Gateway attached to it, to make sure that it has internet connectivity\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourcesToRemove`  <a name="cfn-internetmonitor-monitor-resourcestoremove"></a>
The resources to remove from a monitor, which you provide as a set of Amazon Resource Names \(ARNs\)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-internetmonitor-monitor-status"></a>
The status of a monitor\. The accepted values that you can specify for `Status` are `ACTIVE` and `INACTIVE`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-internetmonitor-monitor-tags"></a>
The tags for a monitor, listed as a set of *key:value* pairs\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-internetmonitor-monitor-return-values"></a>

### Ref<a name="aws-resource-internetmonitor-monitor-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the monitor, such as `arn:aws:internetmonitor:us-east-1:111122223333:monitor/TestMonitor`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-internetmonitor-monitor-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-internetmonitor-monitor-return-values-fn--getatt-fn--getatt"></a>

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The time when the monitor was created\.

`ModifiedAt`  <a name="ModifiedAt-fn::getatt"></a>
The last time that the monitor was modified\.

`MonitorArn`  <a name="MonitorArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the monitor\.

`ProcessingStatus`  <a name="ProcessingStatus-fn::getatt"></a>
The health of data processing for the monitor\. For more information, see `ProcessingStatus` under [ MonitorListMember](https://docs.aws.amazon.com/internet-monitor/latest/api/API_MonitorListMember.html) in the *Amazon CloudWatch Internet Monitor API Reference*\.

`ProcessingStatusInfo`  <a name="ProcessingStatusInfo-fn::getatt"></a>
Additional information about the health of the data processing for the monitor\.