# AWS::Config::ConfigurationRecorder RecordingGroup<a name="aws-properties-config-configurationrecorder-recordinggroup"></a>

Specifies which resource types AWS Config records for configuration changes\. In the recording group, you specify whether you want to record all supported resource types or to include or exclude specific types of resources\.

By default, AWS Config records configuration changes for all supported types of *Regional resources* that AWS Config discovers in the AWS Region in which it is running\. Regional resources are tied to a Region and can be used only in that Region\. Examples of Regional resources are Amazon EC2 instances and Amazon EBS volumes\.

You can also have AWS Config record supported types of *globally recorded resources*\. Globally recorded resource types are not tied to a specific Region and can be used in all Regions\. The globally recorded resource types that AWS Config supports are IAM users, groups, roles, and customer managed policies\. These resource types are recorded in all enabled AWS Config regions where AWS Config was available before February 2022 \(which excludes Asia Pacific \(Hyderabad\), Asia Pacific \(Melbourne\), Europe \(Spain\), Europe \(Zurich\), Israel \(Tel Aviv\), and Middle East \(UAE\)\)\. AWS Config also supports some global resources types for Amazon Elastic Container Registry Public, AWS Global Accelerator, and Amazon Route 53; however, these resource types are not globally recorded in all enabled AWS Config regions\.

**Important**  
Global resource types onboarded to AWS Config recording after February 2022 will be recorded only in the service's home Region for the commercial partition and AWS GovCloud \(US\-West\) for the AWS GovCloud \(US\) partition\. You can view the Configuration Items for these new global resource types only in their home Region and AWS GovCloud \(US\-West\)\.

If you don't want AWS Config to record all resources, you can specify which types of resources AWS Config records with the `resourceTypes` parameter\.

For a list of supported resource types, see [Supported Resource Types](https://docs.aws.amazon.com/config/latest/developerguide/resource-config-reference.html#supported-resources) in the *AWS Config developer guide*\.

For more information and a table of the Home Regions for Global Resource Types Onboarded after February 2022, see [Selecting Which Resources AWS Config Records](https://docs.aws.amazon.com/config/latest/developerguide/select-resources.html) in the *AWS Config developer guide*\.

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
Specifies whether AWS Config records configuration changes for globally recorded resource types \(IAM users, groups, roles, and customer managed policies\)\. These resource types are recorded in all enabled AWS Config regions where AWS Config was available before February 2022 \(which excludes Asia Pacific \(Hyderabad\), Asia Pacific \(Melbourne\), Europe \(Spain\), Europe \(Zurich\), Israel \(Tel Aviv\), and Middle East \(UAE\)\)\.  
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
+ If you set the `useOnly` field of [AWS::Config::ConfigurationRecorder RecordingStrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordingstrategy.html) to `EXCLUSION_BY_RESOURCE_TYPES`, AWS Config records configuration changes for all supported resource types except the resource types that you specify as exemptions to exclude from being recorded in the `resourceTypes` field of [AWS::Config::ConfigurationRecorder ExclusionByResourceTypes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-exclusionbyresourcetypes.html)\.
The `recordingStrategy` field is optional when you set the `allSupported` field of [AWS::Config::ConfigurationRecorder RecordingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordinggroup.html) to `true`\.  
The `recordingStrategy` field is optional when you list resource types in the `resourceTypes` field of [AWS::Config::ConfigurationRecorder RecordingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-recordinggroup.html)\.  
The `recordingStrategy` field is required if you list resource types to exclude from recording in the `resourceTypes` field of [AWS::Config::ConfigurationRecorder ExclusionByResourceTypes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-config-configurationrecorder-exclusionbyresourcetypes.html)\.
If you choose `EXCLUSION_BY_RESOURCE_TYPES` for the recording strategy, the `exclusionByResourceTypes` field will override other properties in the request\.  
For example, even if you set `includeGlobalResourceTypes` to false, global resource types will still be automatically recorded in this option unless those resource types are specifically listed as exemptions in the `resourceTypes` field of `exclusionByResourceTypes`\.  
By default, if you choose the `EXCLUSION_BY_RESOURCE_TYPES` recording strategy, when AWS Config adds support for a new resource type in the Region where you set up the configuration recorder, including global resource types, AWS Config starts recording resources of that type automatically\.
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