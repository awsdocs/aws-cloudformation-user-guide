# AWS::Config::ConfigurationRecorder RecordingGroup<a name="aws-properties-config-configurationrecorder-recordinggroup"></a>

Specifies which AWS resource types AWS Config records for configuration changes\. In the recording group, you specify whether you want to record all supported resource types or only specific types of resources\.

By default, AWS Config records the configuration changes for all supported types of *regional resources* that AWS Config discovers in the region in which it is running\. Regional resources are tied to a region and can be used only in that region\. Examples of regional resources are EC2 instances and EBS volumes\.

You can also have AWS Config record supported types of *global resources*\. Global resources are not tied to a specific region and can be used in all regions\. The global resource types that AWS Config supports include IAM users, groups, roles, and customer managed policies\.

**Important**  
Global resource types onboarded to AWS Config recording after February 2022 will only be recorded in the service's home region for the commercial partition and AWS GovCloud \(US\) West for the GovCloud partition\. You can view the Configuration Items for these new global resource types only in their home region and AWS GovCloud \(US\) West\.  
Supported global resource types onboarded before February 2022 such as `AWS::IAM::Group`, `AWS::IAM::Policy`, `AWS::IAM::Role`, `AWS::IAM::User` remain unchanged, and they will continue to deliver Configuration Items in all supported regions in AWS Config\. The change will only affect new global resource types onboarded after February 2022\.  
To record global resource types onboarded after February 2022, enable All Supported Resource Types in the home region of the global resource type you want to record\.

If you don't want AWS Config to record all resources, you can specify which types of resources it will record with the `resourceTypes` parameter\.

For a list of supported resource types, see [Supported Resource Types](https://docs.aws.amazon.com/config/latest/developerguide/resource-config-reference.html#supported-resources)\.

For more information and a table of the Home Regions for Global Resource Types Onboarded after February 2022, see [Selecting Which Resources AWS Config Records](https://docs.aws.amazon.com/config/latest/developerguide/select-resources.html)\.

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
Specifies whether AWS Config records configuration changes for every supported type of regional resource\.  
If you set this option to `true`, when AWS Config adds support for a new type of regional resource, it starts recording resources of that type automatically\.  
If you set this option to `true`, you cannot enumerate a list of `resourceTypes`\.  
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