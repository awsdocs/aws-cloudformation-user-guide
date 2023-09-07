# AWS::Config::ConfigurationRecorder RecordingGroup<a name="aws-properties-config-configurationrecorder-recordinggroup"></a>

Specifies which resource types AWS Config records for configuration changes\. In the recording group, you specify whether you want to record all supported resource types or to include or exclude specific types of resources\.

**Regional resources**  
By default, AWS Config records configuration changes for all current and future supported types of *Regional resources* that AWS Config discovers in the AWS Region where it is running\. When AWS Config adds support for a new type of Regional resource, AWS Config starts recording resources of that type automatically\.  
Regional resources are tied to a Region and can be used only in that Region\. You create them in a specified AWS Region, and then they exist in that Region\. To see or interact with those resources, you must direct your operations to that Region\. For example, to create an Amazon EC2 instance with the AWS Management Console, you [choose the AWS Region](https://docs.aws.amazon.com/awsconsolehelpdocs/latest/gsg/select-region.html) that you want to create the instance in\. If you use the AWS Command Line Interface \(AWS CLI\) to create the instance, then you include the `--region` parameter\. The AWS SDKs each have their own equivalent mechanism to specify the Region that the operation uses\.  
There are several reasons for using Regional resources\. One reason is to ensure that the resources, and the service endpoints that you use to access them, are as close to the customer as possible\. This improves performance by minimizing latency\. Another reason is to provide an isolation boundary\. This lets you create independent copies of resources in multiple Regions to distribute the load and improve scalability\. At the same time, it isolates the resources from each other to improve availability\.  
If you specify a different AWS Region in the console or in an AWS CLI command, then you can no longer see or interact with the resources you could see in the previous Region\.  
When you look at the [Amazon Resource Name \(ARN\)](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) for a Regional resource, the Region that contains the resource is specified as the fourth field in the ARN\. For example, an Amazon EC2 instance is a Regional resource\. The following is an example of an ARN for a Amazon Virtual Private Cloud \(Amazon VPC\) that exists in the `us-east-1` Region:  
`arn:aws:ec2:us-east-1:123456789012:instance/i-0a6f30921424d3eee`\.

**Global resources**  
Some AWS services resources are *global resources*, meaning that you can use the resource from ***anywhere***\. You don't specify an AWS Region in a global service's console\. To access a global resource, you don't specify a `--region` parameter when using the service's AWS CLI and AWS SDK operations\.  
Global resources support cases where it is critical that only one instance of a particular resource can exist at a time\. In these scenarios, replication or synchronization between copies in different Regions is not adequate\. Having to access a single global endpoint, with the possible increase in latency, is considered acceptable to ensure that any changes are instantaneously visible to consumers of the resource\.  
For example, Amazon Aurora global clusters \(`AWS::RDS::GlobalCluster`\) are global resources, and therefore not tied to a Region\. This means that you can create a global cluster without relying on a regional endpoint\. The benefit is that, while the Amazon Relational Database Service \(Amazon RDS\) itself is organized by Regions, the specific Region where a global cluster originates doesn't impact the global cluster\. It appears as a single, continuous global cluster across all Regions\.  
The [Amazon Resource Name \(ARN\)](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) for a global resource doesn't include a Region\. The fourth field is empty, such as in the following example of an ARN for a global cluster:  
`arn:aws:rds::123456789012:global-cluster:test-global-cluster`\.  
Configuration changes for global resources are recorded by AWS Config in two different ways: 1\) *regionally recorded* in only in the home Region of the global resource or 2\) *globally recorded* in all enabled Regions\.  
**Regionally recorded**  
Global resources for the following services are only recorded in the home Region of the global resource type: Amazon Elastic Container Registry Public, AWS Global Accelerator, and Amazon Route 53\. For these global resources, the same instance of the resource type can be used in multiple AWS Regions, but the configuration items are only recorded in the home Region for the commercial partition or AWS GovCloud \(US\-West\) for the AWS GovCloud \(US\) partition\.  
For a table of the Home Regions for Global Resource Types, see [Selecting Which Resources AWS Config Records](https://docs.aws.amazon.com/config/latest/developerguide/select-resources.html) in the *AWS Config developer guide*\.  
**Globally recorded**  
Globally recorded resource types are recorded in all supported AWS Config Regions where the configuration recorder is enabled\. Currently, there are two types of globally recorded resources: Aurora global clusters and IAM resources\.  
**Aurora global clusters**  
`AWS::RDS::GlobalCluster` is a globally recorded resource type\. It is recorded in all supported Amazon RDS Regions where the configuration recorder is enabled\.  
**IAM resources**  
The following IAM resource types are also globally recorded: IAM users, groups, roles, and customer managed policies\. However, these resource types are only recorded in all supported Amazon RDS Regions where the configuration recorder is enabled and that were supported by AWS Config; *before* February 2022\. This list does not include the following Regions: Asia Pacific \(Hyderabad\), Asia Pacific \(Melbourne\), Europe \(Spain\), Europe \(Zurich\), Israel \(Tel Aviv\), and Middle East \(UAE\)\.  
When you select **Include globally recorded resource types** in the AWS Config console, or input `includeGlobalResourceTypes=true` using the API or CLI, this option only applies to globally recorded resources\. This option does *not* apply to global resources recorded only in a home Region\.

For a list of supported resource types, see [Supported Resource Types](https://docs.aws.amazon.com/config/latest/developerguide/resource-config-reference.html#supported-resources) in the *AWS Config developer guide*\.

**Note**  
If you don't want AWS Config to record all resources, you can specify which types of resources AWS Config records with the `resourceTypes` parameter\.

## Syntax<a name="aws-properties-config-configurationrecorder-recordinggroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-configurationrecorder-recordinggroup-syntax.json"></a>

```
{
  "[AllSupported](#cfn-config-configurationrecorder-recordinggroup-allsupported)" : Boolean,
  "[ExclusionByResourceTypes](#cfn-config-configurationrecorder-recordinggroup-exclusionbyresourcetypes)" : ExclusionByResourceTypes,
  "[IncludeGlobalResourceTypes](#cfn-config-configurationrecorder-recordinggroup-includeglobalresourcetypes)" : Boolean,
  "[RecordingStrategy](#cfn-config-configurationrecorder-recordinggroup-recordingstrategy)" : RecordingStrategy,
  "[ResourceTypes](#cfn-config-configurationrecorder-recordinggroup-resourcetypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-config-configurationrecorder-recordinggroup-syntax.yaml"></a>

```
  [AllSupported](#cfn-config-configurationrecorder-recordinggroup-allsupported): Boolean
  [ExclusionByResourceTypes](#cfn-config-configurationrecorder-recordinggroup-exclusionbyresourcetypes): 
    ExclusionByResourceTypes
  [IncludeGlobalResourceTypes](#cfn-config-configurationrecorder-recordinggroup-includeglobalresourcetypes): Boolean
  [RecordingStrategy](#cfn-config-configurationrecorder-recordinggroup-recordingstrategy): 
    RecordingStrategy
  [ResourceTypes](#cfn-config-configurationrecorder-recordinggroup-resourcetypes): 
    - String
```

## Properties<a name="aws-properties-config-configurationrecorder-recordinggroup-properties"></a>

`AllSupported`  <a name="cfn-config-configurationrecorder-recordinggroup-allsupported"></a>
Specifies whether AWS Config records configuration changes for all supported regional resource types\.  
If you set this field to `true`, when AWS Config adds support for a new type of regional resource, AWS Config starts recording resources of that type automatically\.  
If you set this field to `true`, you cannot enumerate specific resource types to record in the `resourceTypes` field of [RecordingGroup](https://docs.aws.amazon.com/config/latest/APIReference/API_RecordingGroup.html), or to exclude in the `resourceTypes` field of [ExclusionByResourceTypes](https://docs.aws.amazon.com/config/latest/APIReference/API_ExclusionByResourceTypes.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExclusionByResourceTypes`  <a name="cfn-config-configurationrecorder-recordinggroup-exclusionbyresourcetypes"></a>
An object that specifies how AWS Config excludes resource types from being recorded by the configuration recorder\.  
To use this option, you must set the `useOnly` field of [AWS::Config::ConfigurationRecorder RecordingStrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordingstrategy.html) to `EXCLUSION_BY_RESOURCE_TYPES`\.  
*Required*: No  
*Type*: [ExclusionByResourceTypes](aws-properties-config-configurationrecorder-exclusionbyresourcetypes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeGlobalResourceTypes`  <a name="cfn-config-configurationrecorder-recordinggroup-includeglobalresourcetypes"></a>
Specifies whether AWS Config records configuration changes for globally recorded resource types \(`AWS::RDS::GlobalCluster` and IAM users, groups, roles, and customer managed policies\)\. If you select this option, `AWS::RDS::GlobalCluster` will be recorded in all supported AWS Config Regions were the configuration recorder is enabled\. IAM users, groups, roles, and customer managed policies will be recorded in all enabled AWS Config regions where AWS Config was available before February 2022\. This list does not include the following Regions:  
+ Asia Pacific \(Hyderabad\)
+ Asia Pacific \(Melbourne\)
+ Europe \(Spain\)
+ Europe \(Zurich\)
+ Israel \(Tel Aviv\)
+ Middle East \(UAE\)
Before you set this field to `true`, set the `allSupported` field of [AWS::Config::ConfigurationRecorder RecordingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordinggroup.html) to `true`\. Optionally, you can set the `useOnly` field of [AWS::Config::ConfigurationRecorder RecordingStrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordingstrategy.html) to `ALL_SUPPORTED_RESOURCE_TYPES`\.  
If you set this field to `true`, when AWS Config adds support for a new type of global resource in the Region where you set up the configuration recorder, AWS Config starts recording resources of that type automatically\.  
If you set this field to `false` but list global resource types in the `resourceTypes` field of [AWS::Config::ConfigurationRecorder RecordingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordinggroup.html), AWS Config will still record configuration changes for those specified resource types *regardless* of if you set the `includeGlobalResourceTypes` field to false\.  
If you do not want to record configuration changes to global resource types, make sure to not list them in the `resourceTypes` field in addition to setting the `includeGlobalResourceTypes` field to false\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecordingStrategy`  <a name="cfn-config-configurationrecorder-recordinggroup-recordingstrategy"></a>
An object that specifies the recording strategy for the configuration recorder\.  
+ If you set the `useOnly` field of [AWS::Config::ConfigurationRecorder RecordingStrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordingstrategy.html) to `ALL_SUPPORTED_RESOURCE_TYPES`, AWS Config records configuration changes for all supported regional resource types\. You also must set the `allSupported` field of [AWS::Config::ConfigurationRecorder RecordingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordinggroup.html) to `true`\. When AWS Config adds support for a new type of regional resource, AWS Config automatically starts recording resources of that type\.
+ If you set the `useOnly` field of [AWS::Config::ConfigurationRecorder RecordingStrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordingstrategy.html) to `INCLUSION_BY_RESOURCE_TYPES`, AWS Config records configuration changes for only the resource types you specify in the `resourceTypes` field of [AWS::Config::ConfigurationRecorder RecordingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordinggroup.html)\.
+ If you set the `useOnly` field of [AWS::Config::ConfigurationRecorder RecordingStrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordingstrategy.html) to `EXCLUSION_BY_RESOURCE_TYPES`, AWS Config records configuration changes for all supported resource types except the resource types that you specify to exclude from being recorded in the `resourceTypes` field of [AWS::Config::ConfigurationRecorder ExclusionByResourceTypes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-exclusionbyresourcetypes.html)\.
**Required and optional fields**  
The `recordingStrategy` field is optional when you set the `allSupported` field of [AWS::Config::ConfigurationRecorder RecordingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordinggroup.html) to `true`\.  
The `recordingStrategy` field is optional when you list resource types in the `resourceTypes` field of [AWS::Config::ConfigurationRecorder RecordingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordinggroup.html)\.  
The `recordingStrategy` field is required if you list resource types to exclude from recording in the `resourceTypes` field of [AWS::Config::ConfigurationRecorder ExclusionByResourceTypes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-exclusionbyresourcetypes.html)\.
**Overriding fields**  
If you choose `EXCLUSION_BY_RESOURCE_TYPES` for the recording strategy, the `exclusionByResourceTypes` field will override other properties in the request\.  
For example, even if you set `includeGlobalResourceTypes` to false, global resource types will still be automatically recorded in this option unless those resource types are specifically listed as exclusions in the `resourceTypes` field of `exclusionByResourceTypes`\.
**Global resource types and the exclusion recording strategy**  
By default, if you choose the `EXCLUSION_BY_RESOURCE_TYPES` recording strategy, when AWS Config adds support for a new resource type in the Region where you set up the configuration recorder, including global resource types, AWS Config starts recording resources of that type automatically\.  
In addition, unless specifically listed as exclusions, `AWS::RDS::GlobalCluster` will be recorded automatically in all supported AWS Config Regions were the configuration recorder is enabled\. IAM users, groups, roles, and customer managed policies will be recorded automatically in all enabled AWS Config Regions where AWS Config was available before February 2022\. This list does not include the following Regions:  
+ Asia Pacific \(Hyderabad\)
+ Asia Pacific \(Melbourne\)
+ Europe \(Spain\)
+ Europe \(Zurich\)
+ Israel \(Tel Aviv\)
+ Middle East \(UAE\)
*Required*: No  
*Type*: [RecordingStrategy](aws-properties-config-configurationrecorder-recordingstrategy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTypes`  <a name="cfn-config-configurationrecorder-recordinggroup-resourcetypes"></a>
A comma\-separated list that specifies which resource types AWS Config records\.  
Optionally, you can set the `useOnly` field of [AWS::Config::ConfigurationRecorder RecordingStrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordingstrategy.html) to `INCLUSION_BY_RESOURCE_TYPES`\.  
To record all configuration changes, set the `allSupported` field of [AWS::Config::ConfigurationRecorder RecordingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordinggroup.html) to `true`, and either omit this field or don't specify any resource types in this field\. If you set the `allSupported` field to `false` and specify values for `resourceTypes`, when AWS Config adds support for a new type of resource, it will not record resources of that type unless you manually add that type to your recording group\.  
For a list of valid `resourceTypes` values, see the **Resource Type Value** column in [Supported AWS resource Types](https://docs.aws.amazon.com/config/latest/developerguide/resource-config-reference.html#supported-resources) in the *AWS Config developer guide*\.  
**Region Availability**  
Before specifying a resource type for AWS Config to track, check [Resource Coverage by Region Availability](https://docs.aws.amazon.com/config/latest/developerguide/what-is-resource-config-coverage.html) to see if the resource type is supported in the AWS Region where you set up AWS Config\. If a resource type is supported by AWS Config in at least one Region, you can enable the recording of that resource type in all Regions supported by AWS Config, even if the specified resource type is not supported in the AWS Region where you set up AWS Config\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)