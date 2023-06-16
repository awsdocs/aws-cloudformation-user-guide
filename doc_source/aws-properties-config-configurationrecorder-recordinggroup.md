# AWS::Config::ConfigurationRecorder RecordingGroup<a name="aws-properties-config-configurationrecorder-recordinggroup"></a>

Specifies which resource types AWS Config records for configuration changes\. In the recording group, you specify whether you want to record all supported resource types or to include or exclude specific types of resources\.

By default, AWS Config records configuration changes for all supported types of *Regional resources* that AWS Config discovers in the AWS Region in which it is running\. Regional resources are tied to a Region and can be used only in that Region\. Examples of Regional resources are Amazon EC2 instances and Amazon EBS volumes\.

You can also have AWS Config record supported types of *globally recorded resources*\. Globally recorded resource types are not tied to a specific Region and can be used in all Regions\. The globally recorded resource types that AWS Config supports are IAM users, groups, roles, and customer managed policies\. These resource types are recorded in all enabled AWS Config regions\. AWS Config also supports some global resources types for Amazon Elastic Container Registry Public, AWS Global Accelerator, and Amazon Route 53; however, these resource types are not globally recorded in all enabled AWS Config regions\.

**Important**  
Global resource types onboarded to AWS Config recording after February 2022 will be recorded only in the service's home Region for the commercial partition and AWS GovCloud \(US\-West\) for the AWS GovCloud \(US\) partition\. You can view the Configuration Items for these new global resource types only in their home Region and AWS GovCloud \(US\-West\)\.

If you don't want AWS Config to record all resources, you can specify which types of resources AWS Config records with the `resourceTypes` parameter\.

For a list of supported resource types, see [Supported Resource Types](https://docs.aws.amazon.com/config/latest/developerguide/resource-config-reference.html#supported-resources) in the * AWS Config developer guide*\.

For more information and a table of the Home Regions for Global Resource Types Onboarded after February 2022, see [Selecting Which Resources AWS Config Records](https://docs.aws.amazon.com/config/latest/developerguide/select-resources.html) in the * AWS Config developer guide*\.

## Syntax<a name="aws-properties-config-configurationrecorder-recordinggroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-configurationrecorder-recordinggroup-syntax.json"></a>

```
{
  "[AllSupported](#cfn-config-configurationrecorder-recordinggroup-allsupported)" : Boolean,
  "[IncludeGlobalResourceTypes](#cfn-config-configurationrecorder-recordinggroup-includeglobalresourcetypes)" : Boolean,
  "[ResourceTypes](#cfn-config-configurationrecorder-recordinggroup-resourcetypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-config-configurationrecorder-recordinggroup-syntax.yaml"></a>

```
  [AllSupported](#cfn-config-configurationrecorder-recordinggroup-allsupported): Boolean
  [IncludeGlobalResourceTypes](#cfn-config-configurationrecorder-recordinggroup-includeglobalresourcetypes): Boolean
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

`IncludeGlobalResourceTypes`  <a name="cfn-config-configurationrecorder-recordinggroup-includeglobalresourcetypes"></a>
Specifies whether AWS Config includes all supported types of global resources \(for example, IAM resources\) with the resources that it records\.  
Before you can set this option to `true`, you must set the `AllSupported` option to `true`\.  
If you set this option to `true`, when AWS Config adds support for a new type of global resource, it starts recording resources of that type automatically\.  
The configuration details for any global resource are the same in all regions\. To prevent duplicate configuration items, you should consider customizing AWS Config in only one region to record global resources\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTypes`  <a name="cfn-config-configurationrecorder-recordinggroup-resourcetypes"></a>
A comma\-separated list that specifies the types of AWS resources for which AWS Config records configuration changes \(for example, `AWS::EC2::Instance` or `AWS::CloudTrail::Trail`\)\.  
To record all configuration changes, you must set the `AllSupported` option to `false`\.  
If you set the `AllSupported` option to false and populate the `ResourceTypes` option with values, when AWS Config adds support for a new type of resource, it will not record resources of that type unless you manually add that type to your recording group\.  
For a list of valid `resourceTypes` values, see the **resourceType Value** column in [Supported AWS Resource Types](https://docs.aws.amazon.com/config/latest/developerguide/resource-config-reference.html#supported-resources)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)